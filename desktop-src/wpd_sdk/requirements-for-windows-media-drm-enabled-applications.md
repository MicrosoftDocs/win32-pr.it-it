---
description: Requisiti per Windows applicazioni DRM-Enabled multimediali
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Requisiti per Windows applicazioni DRM-Enabled multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14ad59b5b590436ca5734fcb8d226d41f4f995a5d4ea97e0c46d771df476be6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118027050"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Requisiti per Windows applicazioni DRM-Enabled multimediali

Per creare un'applicazione abilitata per Windows Media Digital Rights Management (DRM), è necessario disporre [](general-requirements-for-application-development.md) delle intestazioni e delle librerie descritte nella sezione Requisiti generali per lo sviluppo di applicazioni di questo documento. Inoltre, l'applicazione dovrà fornire proprietà aggiuntive nelle informazioni client all'apertura del dispositivo.

Nella tabella seguente sono descritte le due proprietà aggiuntive necessarie per Windows i trasferimenti di contenuto protetti da Media DRM.



| Proprietà                                      | Descrizione                              |
|-----------------------------------------------|------------------------------------------|
| CHIAVE PRIVATA \_ \_ DELL'APPLICAZIONE WMDRM \_ DEL \_ CLIENT WPD \_ | Specifica la chiave privata dell'applicazione. |
| CERTIFICATO \_ DELL'APPLICAZIONE \_ WMDRM \_ CLIENT \_ WPD  | Specifica il certificato dell'applicazione. |



 

Queste proprietà devono essere fornite nelle informazioni client dell'applicazione quando il dispositivo viene aperto con il [**metodo IPortableDevice::Open.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) Quando vengono fornite queste proprietà, l'API WPD consente il trasferimento di contenuto protetto. Se l'applicazione ha fornito un certificato e una chiave privata, l'API creerà un canale sicuro per trasferire il contenuto WMDRM protetto al dispositivo.

Per informazioni sulla creazione e la distribuzione di applicazioni basate su Windows che supportano Windows Media DRM, vedere l'argomento Licensing [Windows-based Applications (Applicazioni](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) basate su Windows licenze).

## <a name="transferring-content"></a>Trasferimento di contenuto

Per trasferire il contenuto protetto da WMDRM, usare [**IPortableDeviceContent::CreateObjectWithPropertiesAndData.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) Questo metodo può essere usato sia per contenuto protetto che per contenuto non crittografato senza opzioni aggiuntive. L'API WPD selezionerà automaticamente il canale protetto o non crittografato a seconda che il contenuto sia protetto o non crittografato. Si interfaccia con il provider di contenuti protetti WMDRM per elaborare le licenze WMDRM.

## <a name="transferring-known-clear-content"></a>Trasferimento di contenuto non crittografato noto

Se l'applicazione è stata abilitata per la gestione del contenuto protetto, ma si sa che un file specifico non è protetto, è possibile indicare a WPD di ignorare l'elaborazione DRM impostando **l'opzione DELL'API WPD \_ USE CLEAR DATA \_ \_ \_ \_ \_ STREAM** su TRUE nell'input **IPortableDeviceValues** quando si chiama [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) per cancellare il contenuto.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Accesso alle operazioni di misurazione tramite IWMDRMDeviceApp

WPD fornisce un meccanismo per accedere alle **API IWMDRMDeviceApp** per gli aggiornamenti delle licenze e il recupero dei dati di misurazione. Per accedere a questa API tramite WPD, chiamare **QueryInterface** su **\_ IID IWMDRMDeviceApp** dall'oggetto **IStream** restituito da [**IPortableDeviceContent::CreateObjectWithPropertiesAndData.**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) Questa **istanza di IWMDRMDeviceApp** associata alla connessione **IPortableDevice** al dispositivo compatibile con WMDRM e non al contenuto specifico in cui è stato **ottenuto il flusso IStream.** WPD esegue internamente il wrapping delle API di misurazione e la rende accessibile all'applicazione. L'applicazione deve usare la costante PTR DEL DISPOSITIVO \_ WMDRMDEVICEAPP USE WPD per il \_ parametro \_ \_ *IWMDMDevice.* \*

Il frammento di codice seguente illustra questa operazione.


```C++
IStream*               pDataStream = NULL;

IWMDRMDeviceApp*       pWMDRMApp   = NULL;

  

// ... Initialization 

 

hr = pPortableDeviceContent->CreateObjectWithPropertiesAndData(pValues,

                              &pDataStream,

                              &dwOptimalWriteBufferSize,

                              NULL);

 

// ... Transfer the protected WMDRM content 

pDataStream->Write(pData, cbData, &cbWritten);

 

pDataStream->Commit(0);

 

hr = pDataStream->QueryInterface(IID_IWMDRMDeviceApp, 

                                 (void**)&pWMDRMApp);

 

if (SUCCEEDED(hr))

{

   DWORD dwStatus = 0;

 

   // Call metering operations on the current device using the WPD device pointer

   hr = pWMDRMApp->QueryDeviceStatus((IWMDMDevice *)WMDRMDEVICEAPP_USE_WPD_DEVICE_PTR, 

                                     &dwStatus);

}

```



Anche in questo caso si applica lo stesso requisito con la chiave privata dell'applicazione e il certificato. Se la chiave/certificato non è valido o se l'inizializzazione del sistema WMDRM non riesce, la **chiamata a QueryInferface** avrà esito negativo.

Il metodo precedente per acquisire l'interfaccia **IWMDRMDeviceApp** dal puntatore **IStream** è semplicemente un'operazione utile se l'applicazione sta già eseguendo un trasferimento del contenuto protetto precedente, prima di procedere con le operazioni di misurazione e sincronizzazione delle licenze.

Per la maggior parte delle applicazioni che devono accedere a **IWMDRMDeviceApp** è consigliabile inizializzare **IWMDRMDeviceApp** direttamente, in quanto ciò non richiede all'applicazione di trasferire contenuto protetto o di mantenere le interfacce di trasferimento per eseguire la misurazione del dispositivo e la sincronizzazione delle licenze. Questo metodo richiederà l'Windows delle API di Gestione dispositivi multimediali (WMDM). Per informazioni dettagliate e codice di esempio, vedere il white paper [Accessing WMDRM APIs from a WPD Application](../windows-portable-devices.md) (Accesso alle API WMDRM da un'applicazione WPD) nel sito WHDC.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Windows Dispositivi portatili**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
