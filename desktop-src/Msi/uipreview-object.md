---
description: L'oggetto UIPreview viene usato per visualizzare finestre di dialogo e finestre di dialogo dell'interfaccia utente durante la creazione. Questo oggetto viene creato dal metodo EnableUIPreview dell'oggetto Database.
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
ms.openlocfilehash: 82436f21cc3920c2e1f635f8d1612118831e7d29f3fb1202105511f2e61f7a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118623500"
---
# <a name="uipreview-object"></a>Oggetto UIPreview

**L'oggetto UIPreview** viene usato per visualizzare finestre di dialogo e finestre di dialogo dell'interfaccia utente durante la creazione. Questo oggetto viene creato dal [**metodo EnableUIPreview**](database-enableuipreview.md) dell'oggetto [**Database.**](database-object.md)

## <a name="members"></a>Membri

**L'oggetto UIPreview** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto UIPreview** dispone di questi metodi.



| Metodo                                           | Descrizione                                                                                             |
|:-------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**ViewBillboard**](uipreview-viewbillboard.md) | Visualizza un oggetto creato utilizzando il controllo host nella finestra di dialogo attualmente visualizzata.<br/> |
| [**Finestra di dialogo Visualizza**](uipreview-viewdialog.md)       | Visualizza una finestra di dialogo dell'interfaccia utente personalizzata archiviata nel database corrente.<br/>                           |



 

### <a name="properties"></a>Proprietà

**L'oggetto UIPreview** ha queste proprietà.



| Proprietà                                          | Tipo di accesso           | Descrizione                                                                                                                                                                       |
|:--------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Proprietà**](uipreview-property.md)<br/> | Lettura/Scrittura<br/> | Rappresenta il valore stringa di una proprietà del programma di installazione denominata o, se preceduto da un segno di percentuale (%), il valore di una variabile di ambiente di sistema per il processo corrente.<br/> |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IUIPreview è definito come 000C109A-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Windows Esempi di script del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




