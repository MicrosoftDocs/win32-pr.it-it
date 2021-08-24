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
ms.openlocfilehash: 3efdc009f40f0bce67559d185afb4cba1289c00fc1d7771a43d392601220dbae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039591"
---
# <a name="summaryinfo-object"></a>Oggetto SummaryInfo

**L'oggetto SummaryInfo** viene usato per leggere, creare e aggiornare le proprietà del documento dal flusso [di informazioni](summary-information-stream.md) di riepilogo di un oggetto di archiviazione.

## <a name="members"></a>Membri

**L'oggetto SummaryInfo** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto SummaryInfo** dispone di questi metodi.



| Metodo                                 | Descrizione                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Persistono**](summaryinfo-persist.md) | Formatta e scrive le proprietà archiviate in precedenza nel flusso di [informazioni di riepilogo standard.](summary-information-stream.md)<br/> |



 

### <a name="properties"></a>Proprietà

**L'oggetto SummaryInfo** ha queste proprietà.



| Proprietà                                                                             | Descrizione                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Proprietà Property (oggetto SummaryInfo)**](summaryinfo-summaryinfo.md)<br/> | Ottiene o imposta il valore per la proprietà specificata nel flusso di informazioni di riepilogo.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Indica il numero corrente di valori di proprietà nell'oggetto informazioni di riepilogo.<br/>   |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo è definito come 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Proprietà SummaryInformation (oggetto Database)**](database-summaryinformation.md)
</dt> <dt>

[**Proprietà SummaryInformation (oggetto Installer)**](installer-summaryinformation.md)
</dt> <dt>

[Windows Esempi di script del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




