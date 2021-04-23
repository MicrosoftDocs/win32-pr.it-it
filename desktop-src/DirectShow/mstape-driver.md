---
description: MSTape Driver
ms.assetid: aa59f322-09b1-4b0a-be6f-d865c20f76e5
title: MSTape Driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 951084f8827f925bba43028c0792736883d5ff0f
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909399"
---
# <a name="mstape-driver"></a>MSTape Driver

Questo argomento si applica a Windows XP o versioni successive.

Il driver MSTape supporta i dispositivi videocamere D-VHS e MPEG. Viene esposto alle applicazioni come filtro [di acquisizione video WDM.](wdm-video-capture-filter.md) La sua funzionalità è simile a quella di [MSDV,](msdv-driver.md)il driver del videocamere DV:

-   Viene visualizzato nelle categorie di filtro "Video Capture Sources" (CLSID \_ VideoInputDeviceCategory) e "WDM Streaming Rendering Devices" (AM \_ KSCATEGORY \_ RENDER).
-   Un'applicazione può creare un'istanza del filtro usando [**l'interfaccia ICreateDevEnum.**](/windows/desktop/api/Strmif/nn-strmif-icreatedevenum)
-   Include un pin di output per l'acquisizione e il trasporto dal dispositivo e un pin di input per il trasporto al dispositivo. È possibile collegare un solo pin alla volta.

**Tipi di supporti**

Il pin di input supporta un tipo di supporto.



| Label | Valore |
|--------------|------------------------------------------------------------|
| Tipo principale   | Flusso \_ MEDIATYPE                                          |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE                     |
| Dimensione del campione  | 192 x 256                                                  |
| Formatta blocco | [**MPEG2 \_ TRANSPORT \_ STRIDE**](mpeg2-transport-stride.md) |



 

Il pin di output supporta due tipi di supporti.



| Label | Valore |
|--------------|----------------------------------------|
| Tipo principale   | Flusso \_ MEDIATYPE                      |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE |
| Dimensione del campione  | 192 x 256                              |
| Blocco di formato | MPEG2 \_ TRANSPORT \_ STRIDE               |



 



| Label | Valore |
|--------------|----------------------------------------|
| Tipo principale   | Flusso \_ MEDIATYPE                      |
| Subtype      | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE |
| Dimensione del campione  | 188 x 256                              |
| Blocco di formato | **NULL**                               |



 

**Informazioni sul dispositivo**

Il driver legge dinamicamente le informazioni dalla ROM di configurazione del dispositivo. L'applicazione può recuperare queste informazioni associando il moniker del dispositivo a un contenitore di proprietà e chiamando il **metodo IPropertyBag::Read.**



| Proprietà            | Descrizione                                                                                                                                                                         | Tipo di dati           |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| UniqueID \_ Low       | ID univoco del dispositivo **(DWORD basso).**                                                                                                                                            | **long** (VT \_ I4)   |
| UniqueID \_ High      | ID univoco del dispositivo **(DWORD alto)**                                                                                                                                            | **long**            |
| VendorID            | ID fornitore.                                                                                                                                                                          | **long**            |
| ModelID             | ID modello.                                                                                                                                                                           | **long**            |
| Testo fornitore          | Nome del fornitore.                                                                                                                                                                        | **BSTR** (VT \_ BSTR) |
| Testo modello           | Nome del modello di dispositivo.                                                                                                                                                                  | **BSTR**            |
| UnitModelText       | Nome del modello di unità; può essere uguale a ModelText.                                                                                                                                      | **BSTR**            |
| DeviceOPcr0Payload  | Payload oPCR (Output Plug Control). Esempio: 146 quadlet.                                                                                                                          | **long**            |
| DeviceOPcr0DataRate | Frequenza dei dati oPCR. Esempi: 0 (S100), 1 (S200) o 2 (S400).                                                                                                                          | **long**            |
| DeviceClassGUID     | GUID che identifica il driver di dispositivo. Per MSTape, questo valore è `{8C0F6AF2-0EDB-44C1-8AEB-59040BD830ED}` . Questo GUID è definito come MSTapeDeviceGUID nel file di intestazione Xprtdefs.h. | **BSTR**            |
| Descrizione         | Descrizione del dispositivo, tratto dal file INF. Questa stringa contiene in genere il nome del marchio del dispositivo.                                                                    | **BSTR**            |



 

L'ID dispositivo è un intero a 64 bit. Il **valore DWORD basso** viene archiviato nella proprietà UniqueID Low e il valore DWORD alto viene archiviato \_ nella proprietà UniqueID  \_ High.

Per altre informazioni sui moniker dei dispositivi, vedere [Uso dell'enumeratore dispositivo di sistema](using-the-system-device-enumerator.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Filtri DirectShow](directshow-filters.md)
</dt> <dt>

[Controllo di un camcorder DV](controlling-a-dv-camcorder.md)
</dt> </dl>

 

 



