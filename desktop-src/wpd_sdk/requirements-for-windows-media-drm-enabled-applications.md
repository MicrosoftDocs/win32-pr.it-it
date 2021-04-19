---
description: Requisiti per le applicazioni Windows Media DRM-Enabled
ms.assetid: 67f872dc-79ef-4799-bb7b-b84d7dc11c71
title: Requisiti per le applicazioni Windows Media DRM-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59543bf6ea803d2b9d58721fd775c49b79653c0b
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320750"
---
# <a name="requirements-for-windows-media-drm-enabled-applications"></a>Requisiti per le applicazioni Windows Media DRM-Enabled

Per creare un'applicazione Windows Media Digital Rights Management (DRM) abilitata, è necessario disporre delle intestazioni e delle librerie descritte nella sezione [requisiti generali per lo sviluppo di applicazioni](general-requirements-for-application-development.md) di questo documento. Inoltre, quando si apre il dispositivo, l'applicazione dovrà fornire proprietà aggiuntive nelle informazioni sul client.

Nella tabella seguente sono descritte le due proprietà aggiuntive necessarie per abilitare i trasferimenti di contenuto protetti da DRM di Windows Media.



| Proprietà                                      | Descrizione                              |
|-----------------------------------------------|------------------------------------------|
| \_ \_ \_ chiave privata dell'applicazione \_ WMDRM \_ client WPD | Specifica la chiave privata dell'applicazione. |
| \_ \_ \_ certificato applicazione WMDRM client \_ WPD  | Specifica il certificato dell'applicazione. |



 

Queste proprietà devono essere specificate nelle informazioni sul client dell'applicazione quando il dispositivo viene aperto con il metodo [**IPortableDevice:: Open**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-open) . Quando queste proprietà vengono fornite, l'API WPD consente i trasferimenti di contenuto protetti. Se l'applicazione ha fornito un certificato e una chiave privata, l'API creerà un canale sicuro per trasferire il contenuto WMDRM protetto al dispositivo.

Per informazioni sulla creazione e la distribuzione di applicazioni basate su Windows che supportano Windows Media DRM, vedere l'argomento relativo alle [applicazioni basate su Windows licensing](https://www.microsoft.com/windows/windowsmedia/licensing/licensing_drm_apps.aspx) .

## <a name="transferring-content"></a>Trasferimento di contenuto

Per trasferire il contenuto protetto con WMDRM, usare [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Questo metodo può essere utilizzato sia per il contenuto protetto che per quello non crittografato senza opzioni aggiuntive. L'API WPD seleziona automaticamente il canale protetto o non crittografato, a seconda che il contenuto sia protetto o deselezionato. Si interfaccia con il provider di contenuti WMDRM sicuro per elaborare le licenze WMDRM.

## <a name="transferring-known-clear-content"></a>Trasferimento di contenuto chiaro noto

Se l'applicazione è stata abilitata per la gestione del contenuto protetto, ma si sa che un file specifico non è protetto, è possibile indicare a WPD di ignorare l'elaborazione DRM impostando l' **\_ opzione API WPD usa l'opzione \_ \_ \_ Cancella \_ \_ flusso di dati** su true nell'input **IPortableDeviceValues** quando si chiama [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata) per il contenuto non crittografato.

## <a name="accessing-metering-operations-using-iwmdrmdeviceapp"></a>Accesso alle operazioni di misurazione mediante IWMDRMDeviceApp

WPD fornisce un meccanismo per accedere alle API **IWMDRMDeviceApp** per gli aggiornamenti delle licenze e il recupero dei dati di misurazione. Per accedere a questa API tramite WPD, chiamare **QueryInterface** su **IID \_ IWMDRMDeviceApp** da **IStream** restituito da [**IPortableDeviceContent:: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata). Questa istanza di **IWMDRMDeviceApp** è associata alla connessione **IPortableDevice** al dispositivo compatibile con WMDRM e non al contenuto specifico in cui è stato ottenuto il **IStream** . WPD esegue internamente il wrapping delle API di misurazione e le rende accessibili per l'applicazione. L'applicazione deve usare WMDRMDEVICEAPP \_ per usare \_ la \_ costante PTR del dispositivo WPD \_ per il parametro *IWMDMDevice* \* .

Il frammento di codice seguente illustra questo problema.


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



Lo stesso prerequisito con la chiave privata dell'applicazione e il certificato si applica anche qui. Se la chiave o il certificato non è valido o l'inizializzazione del sistema WMDRM non riesce, la chiamata **QueryInferface** avrà esito negativo.

Il metodo precedente per acquisire l'interfaccia **IWMDRMDeviceApp** dal puntatore **IStream** è semplicemente una praticità se l'applicazione sta già eseguendo un trasferimento di contenuto protetto precedente, prima di procedere con le operazioni di misurazione e sincronizzazione delle licenze.

Il suggerimento per la maggior parte delle applicazioni che devono accedere a **IWMDRMDeviceApp** è l'inizializzazione diretta di **IWMDRMDeviceApp** in quanto questa operazione non richiede che l'applicazione trasferisca contenuti protetti o mantenga le interfacce di trasferimento per eseguire la misurazione dei dispositivi e la sincronizzazione delle licenze. Questo metodo richiede l'utilizzo di API Windows Media Gestione dispositivi (WMDM). Per informazioni dettagliate e per il codice di esempio, vedere il white paper relativo all' [accesso alle API WMDRM da un WPD dell'applicazione](../windows-portable-devices.md) nel sito di whdc.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Dispositivi portatili Windows**](/windows/desktop/windows-portable-devices)
</dt> </dl>

 

 
