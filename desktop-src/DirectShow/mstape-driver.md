---
description: Driver MSTape
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: Driver MSTape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f37e22c26866fca9519219d358e9733fb56151
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103875982"
---
# <a name="mstape-driver"></a>Driver MSTape

Questo argomento si applica a Windows XP o versione successiva.

Il driver MSTape supporta i dispositivi con videocamera D-VHS e MPEG. Viene esposto alle applicazioni come filtro di [acquisizione video WDM](wdm-video-capture-filter.md) . La relativa funzionalità è simile a quella di [Msdv](msdv-driver.md), il driver della videocamera DV:

-   Viene visualizzato nelle categorie di filtri "video Capture Sources" (CLSID \_ VideoInputDeviceCategory) e "WDM Streaming rendering Devices" ( \_ KSCATEGORY \_ Render).
-   Un'applicazione può creare un'istanza del filtro usando l'interfaccia [**ICreateDevEnum**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum) .
-   Include un pin di output per l'acquisizione e il trasporto dal dispositivo e un pin di input per il trasporto al dispositivo. È possibile connettere un solo pin alla volta.

**Tipi di supporto**

Il pin di input supporta un tipo di supporto.



|              |                                                            |
|--------------|------------------------------------------------------------|
| Tipo principale   | \_Flusso MEDIATYPE                                          |
| Subtype      | \_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE                     |
| Dimensione del campione  | 192 x 256                                                  |
| Formato blocco | [**\_Stride trasporto \_ MPEG2**](mpeg2-transport-stride.md) |



 

Il pin di output supporta due tipi di supporto.



|              |                                        |
|--------------|----------------------------------------|
| Tipo principale   | \_Flusso MEDIATYPE                      |
| Subtype      | \_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE |
| Dimensione del campione  | 192 x 256                              |
| Formato blocco | \_Stride trasporto \_ MPEG2               |



 



|              |                                        |
|--------------|----------------------------------------|
| Tipo principale   | \_Flusso MEDIATYPE                      |
| Subtype      | \_ \_ Stride trasporto MPEG2 \_ MEDIASUBTYPE |
| Dimensione del campione  | 188 x 256                              |
| Formato blocco | **NULL**                               |



 

**Informazioni sul dispositivo**

Il driver legge dinamicamente le informazioni dalla ROM di configurazione del dispositivo. L'applicazione può recuperare queste informazioni associando il moniker del dispositivo a un contenitore delle proprietà e chiamando il metodo **IPropertyBag:: Read** .



| Proprietà            | Descrizione                                                                                                                                                                         | Tipo di dati           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueID \_ basso       | ID univoco del dispositivo ( **DWORD** basso).                                                                                                                                            | **Long** (VT \_ I4)   |
| UniqueID \_ alto      | ID univoco del dispositivo ( **DWORD** alto)                                                                                                                                            | **long**            |
| VendorID            | ID fornitore.                                                                                                                                                                          | **long**            |
| ModelID             | ID modello.                                                                                                                                                                           | **long**            |
| VendorText          | Nome del fornitore.                                                                                                                                                                        | **BSTR** (VT \_ BSTR) |
| ModelText           | Nome del modello del dispositivo.                                                                                                                                                                  | **BSTR**            |
| UnitModelText       | Nome del modello di unità; può corrispondere a ModelText.                                                                                                                                      | **BSTR**            |
| DeviceOPcr0Payload  | payload oPCR (controllo plug di output). Esempio: 146 quadlets.                                                                                                                          | **long**            |
| DeviceOPcr0DataRate | velocità dati oPCR. Esempi: 0 (S100), 1 (S200) o 2 (S400).                                                                                                                          | **long**            |
| DeviceClassGUID     | GUID che identifica il driver di dispositivo. Per MSTape, questo valore è `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` . Questo GUID viene definito come MSTapeDeviceGUID nel file di intestazione Xprtdefs. h. | **BSTR**            |
| Descrizione         | Una descrizione del dispositivo, ricavata dal file INF. Questa stringa contiene in genere il nome del marchio del dispositivo.                                                                    | **BSTR**            |



 

L'ID del dispositivo è un Integer a 64 bit. Il **valore DWORD** basso viene archiviato nella proprietà con valore UniqueID \_ basso e il **valore DWORD** elevato viene archiviato nella \_ Proprietà alta UniqueId.

Per ulteriori informazioni sui moniker dei dispositivi, vedere [using the System Device Enumerator](using-the-system-device-enumerator.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Controllo di una videocamera DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



