---
description: L'oggetto UIPreview viene utilizzato per visualizzare le finestre di dialogo e i manifesti dell'interfaccia utente durante la creazione. Questo oggetto viene creato dal metodo EnableUIPreview dell'oggetto di database.
ms.assetid: 5df2a4f3-6352-4575-b822-1811150a86be
title: Oggetto UIPreview
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UIPreview
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 6650dc9bcc66a24d0e8a9d7f0d971884a2379f60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327917"
---
# <a name="uipreview-object"></a>Oggetto UIPreview

L'oggetto **UIPreview** viene utilizzato per visualizzare le finestre di dialogo e i manifesti dell'interfaccia utente durante la creazione. Questo oggetto viene creato dal metodo [**EnableUIPreview**](database-enableuipreview.md) dell'oggetto di [**database**](database-object.md) .

## <a name="members"></a>Membri

L'oggetto **UIPreview** dispone di questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

L'oggetto **UIPreview** dispone di questi metodi.



| Metodo                                           | Descrizione                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | Consente di visualizzare un Billboard creato utilizzando il controllo host nella finestra di dialogo attualmente visualizzata.<br/> |
| [**ViewDialog**](uipreview-viewdialog.md)       | Consente di visualizzare una finestra di dialogo dell'interfaccia utente creata archiviata nel database corrente.<br/>                           |



 

### <a name="properties"></a>Proprietà

L'oggetto **UIPreview** dispone di queste proprietà.



| Proprietà                                          | Tipo di accesso           | Descrizione                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Proprietà**](uipreview-property.md)<br/> | Lettura/Scrittura<br/> | Rappresenta il valore stringa di una proprietà del programma di installazione denominata o, se preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




