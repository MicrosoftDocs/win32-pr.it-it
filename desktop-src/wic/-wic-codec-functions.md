---
title: Funzioni WIC
description: In questa sezione vengono fornite informazioni sulle funzioni di Windows Imaging Component (WIC).
ms.assetid: 6f948df6-5b70-4f1e-b01d-3841d7819acb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25ce53f51f439ab5d0a697c824a1d37db7fd755f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879122"
---
# <a name="wic-functions"></a>Funzioni WIC

In questa sezione vengono fornite informazioni sulle funzioni di Windows Imaging Component (WIC).

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                      | Descrizione                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [*ProgressNotificationCallback*](/windows/desktop/api/Wincodec/nc-wincodec-pfnprogressnotification)<br/>   | Funzione di callback definita dall'applicazione chiamata quando viene eseguito lo stato del componente codec.<br/>                                                                                                                        |
| [**WICConvertBitmapSource**](/windows/desktop/api/Wincodec/nf-wincodec-wicconvertbitmapsource)<br/>             | Ottiene un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) nel formato pixel desiderato da un **IWICBitmapSource** specificato.<br/>                                                                           |
| [**WICCreateBitmapFromSection**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsection)<br/>     | Restituisce un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) supportato dai pixel di un handle di sezione di Windows Graphics Device Interface (GDI).<br/>                                                |
| [**WICCreateBitmapFromSectionEx**](/windows/desktop/api/Wincodec/nf-wincodec-wiccreatebitmapfromsectionex)<br/> | Restituisce un [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) supportato dai pixel di un handle di sezione GDI.<br/>                                                                                    |
| [**WICGetMetadataContentSize**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicgetmetadatacontentsize)<br/>       | Restituisce le dimensioni del contenuto dei metadati contenuti nel [**IWICMetadataWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatawriter)specificato. Gli account di ridimensionamento restituiti per l'intestazione e la lunghezza dei metadati.<br/> |
| [**WICMapGuidToShortName**](/windows/desktop/api/WinCodec/nf-wincodec-wicmapguidtoshortname)<br/>               | Ottiene il nome breve associato a un GUID specificato.<br/>                                                                                                                                                       |
| [**WICMapSchemaToName**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapschematoname)<br/>                     | Ottiene il nome associato a uno schema specificato.<br/>                                                                                                                                                           |
| [**WICMapShortNameToGuid**](/windows/desktop/api/Wincodec/nf-wincodec-wicmapshortnametoguid)<br/>               | Ottiene il GUID associato al nome breve specificato.<br/>                                                                                                                                                     |
| [**WICMatchMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicmatchmetadatacontent)<br/>           | Ottiene un GUID del formato dei metadati per un formato di contenitore e un fornitore che corrisponde meglio al contenuto all'interno di un flusso specificato.<br/>                                                                            |
| [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent)<br/>   | Scrive i metadati in un flusso specificato.<br/>                                                                                                                                                                       |
| [Funzioni proxy WIC](wic-proxy-functions.md)<br/>                                  | In questa sezione sono contenute le funzioni proxy WIC.<br/>                                                                                                                                                             |



 

 

 




