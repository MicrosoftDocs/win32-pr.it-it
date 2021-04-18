---
description: L'oggetto SummaryInfo viene usato per leggere, creare e aggiornare le proprietà del documento dal flusso di informazioni di riepilogo di un oggetto di archiviazione.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: Oggetto SummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329244"
---
# <a name="summaryinfo-object"></a>Oggetto SummaryInfo

L'oggetto **SummaryInfo** viene usato per leggere, creare e aggiornare le proprietà del documento dal [flusso di informazioni di riepilogo](summary-information-stream.md) di un oggetto di archiviazione.

## <a name="members"></a>Membri

L'oggetto **SummaryInfo** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **SummaryInfo** dispone di questi metodi.



| Metodo                                 | Descrizione                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Rendere persistenti**](summaryinfo-persist.md) | Formatta e scrive le proprietà archiviate in precedenza nel [flusso di informazioni di riepilogo](summary-information-stream.md)standard.<br/> |



 

### <a name="properties"></a>Proprietà

L'oggetto **SummaryInfo** dispone di queste proprietà.



| Proprietà                                                                             | Descrizione                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Proprietà Property (oggetto SummaryInfo)**](summaryinfo-summaryinfo.md)<br/> | Ottiene o imposta il valore per la proprietà specificata nel flusso di informazioni di riepilogo.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Indica il numero corrente di valori di proprietà nell'oggetto informazioni di riepilogo.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo è definito come 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà SummaryInformation (oggetto di database)**](database-summaryinformation.md)
</dt> <dt>

[**Proprietà SummaryInformation (oggetto Installer)**](installer-summaryinformation.md)
</dt> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




