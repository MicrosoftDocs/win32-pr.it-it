---
description: L'oggetto ComponentInfo rappresenta informazioni aggiuntive su un componente che può essere ottenuto tramite una chiamata da MsiGetComponentPathEx.
ms.assetid: 9b0ad0a1-c49f-4b14-817b-0cfc9b228d77
title: Oggetto ComponentInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ComponentInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1890ff127f60188deae8fdad251e44b3edb614f7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328013"
---
# <a name="componentinfo-object"></a>Oggetto ComponentInfo

L'oggetto ComponentInfo rappresenta informazioni aggiuntive su un componente che può essere ottenuto tramite una chiamata da MsiGetComponentPathEx.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questo oggetto è disponibile a partire da Windows Installer 5,0.

## <a name="members"></a>Membri

L'oggetto **ComponentInfo** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **ComponentInfo** dispone di queste proprietà.



| Proprietà                                                        | Descrizione                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | Codice del componente in questione.<br/> |
| [**Percorso**](componentinfo-componentcode.md)<br/>          | Percorso del componente.<br/>                       |
| [**State**](componentinfo-state.md)<br/>                 | Stato del componente.<br/>                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 o versione successiva.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponentInfo è definito come 000C1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso dell'interfaccia di automazione](using-the-automation-interface.md)
</dt> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




