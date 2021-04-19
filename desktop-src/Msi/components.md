---
description: L'oggetto Component rappresenta un'istanza univoca di un componente disponibile per l'enumerazione.
ms.assetid: cdc99bc3-9e2a-49db-8c01-b9634aefac38
title: Oggetto Component
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Component
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5e31d6a7c3d2422111d0d8c3247e022fa35bdc43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328012"
---
# <a name="component-object"></a>Oggetto Component

L'oggetto Component rappresenta un'istanza univoca di un componente disponibile per l'enumerazione.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questo oggetto è disponibile a partire da Windows Installer 5,0.

## <a name="members"></a>Membri

L'oggetto **Component** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **Component** dispone di queste proprietà.



| Proprietà                                                    | Descrizione                                                                               |
|:------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**ComponentCode**](component-componentcode.md)<br/> | Codice del componente in questione.<br/>                               |
| [**Context**](component-context.md)<br/>             | Contesto che è stato determinato come applicabile al componente in questione.<br/> |
| [**UserSID**](component-usersid.md)<br/>             | SID utente per il componente enumerato.<br/>                                     |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 o versione successiva.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponent è definito come 000C1097-0000-0000-C000-000000000046<br/>      |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso dell'interfaccia di automazione](using-the-automation-interface.md)
</dt> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




