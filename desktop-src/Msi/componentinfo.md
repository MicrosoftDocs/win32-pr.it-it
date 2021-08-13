---
description: L'oggetto ComponentInfo rappresenta dettagli aggiuntivi su un componente che possono essere ottenuti tramite una chiamata da MsiGetComponentPathEx.
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
ms.openlocfilehash: a59aa1d9f7bdc5babc29461ca90c01b6fe604482cb78ba6549e782b1e34d54b5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119252001"
---
# <a name="componentinfo-object"></a>Oggetto ComponentInfo

L'oggetto ComponentInfo rappresenta dettagli aggiuntivi su un componente che possono essere ottenuti tramite una chiamata da MsiGetComponentPathEx.

**[Windows Installer 4.5 o versioni precedenti:](not-supported-in-windows-installer-4-5.md)** Non supportato. Questo oggetto è disponibile a partire da Windows Installer 5.0.

## <a name="members"></a>Membri

**L'oggetto ComponentInfo** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

**L'oggetto ComponentInfo** ha queste proprietà.



| Proprietà                                                        | Descrizione                                                 |
|:----------------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](componentinfo-componentcode.md)<br/> | Codice del componente in questione.<br/> |
| [**Percorso**](componentinfo-componentcode.md)<br/>          | Percorso del componente.<br/>                       |
| [**Stato**](componentinfo-state.md)<br/>                 | Stato del componente.<br/>                      |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 o versione successiva.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IComponentInfo è definito come 000C1099-0000-0000-C000-000000000046<br/>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso dell'interfaccia di automazione](using-the-automation-interface.md)
</dt> <dt>

[Windows Esempi di script del programma di installazione](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




