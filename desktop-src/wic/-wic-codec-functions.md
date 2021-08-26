---
title: Funzioni WIC
description: Questa sezione contiene informazioni sulle funzioni Windows Imaging Component (WIC).
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f60660780e97831a77101c15646385d62048f005279b388a532ca687a200996
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056801"
---
# <a name="wic-functions"></a>Funzioni WIC

Questa sezione contiene informazioni sulle funzioni Windows Imaging Component (WIC).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                      | Descrizione                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*ProgressNotificationCallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Funzione di callback definita dall'applicazione chiamata quando viene eseguito lo stato del componente codec.<br/>                                                                                                                        |
| [**WICConvertBitmapSource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Ottiene un [**oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) nel formato pixel desiderato da un **oggetto IWICBitmapSource specificato.**<br/>                                                                           |
| [**WICCreateBitmapFromSection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | Restituisce un [**oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) supportato dai pixel di un handle Windows Graphics Device Interface (GDI).<br/>                                                |
| [**WICCreateBitmapFromSectionEx**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Restituisce un [**oggetto IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) supportato dai pixel di un handle di sezione GDI.<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Restituisce le dimensioni del contenuto dei metadati contenuti [**nell'oggetto IWICMetadataWriter specificato.**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter) La dimensione restituita rappresenta l'intestazione e la lunghezza dei metadati.<br/> |
| [**WICMapGuidToShortName**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Ottiene il nome breve associato a un GUID specificato.<br/>                                                                                                                                                       |
| [**WICMapSchemaToName**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Ottiene il nome associato a un determinato schema.<br/>                                                                                                                                                           |
| [**WICMapShortNameToGuid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Ottiene il GUID associato al nome breve specificato.<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Ottiene un GUID del formato di metadati per un formato di contenitore e un fornitore specificati che meglio corrisponde al contenuto all'interno di un flusso specificato.<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Scrive i metadati in un flusso specificato.<br/>                                                                                                                                                                       |
| [Funzioni proxy WIC](wic-proxy-functions.md)<br/>                                  | Questa sezione contiene le funzioni proxy WIC.<br/>                                                                                                                                                             |



 

 

 




