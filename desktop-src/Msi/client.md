---
description: L'oggetto client rappresenta una relazione tra un componente e un prodotto client.
ms.assetid: ac1fbd74-fbc4-4f76-8e14-af48443a8528
title: Oggetto client
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Client
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75cb21a4149d8e6758ab24796949777b8052b120
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328438"
---
# <a name="client-object"></a>Oggetto client

L'oggetto client rappresenta una relazione tra un componente e un prodotto client.

**[Windows Installer 4,5 o versioni precedenti](not-supported-in-windows-installer-4-5.md):** Non supportato. Questo oggetto è disponibile a partire da Windows Installer 5,0.

## <a name="members"></a>Membri

L'oggetto **client** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

L'oggetto **client** dispone di queste proprietà.



| Proprietà                                                 | Descrizione                                                 |
|:---------------------------------------------------------|:------------------------------------------------------------|
| [**ComponentCode**](client-componentcode.md)<br/> | Codice del componente in questione.<br/> |
| [**Context**](client-context.md)<br/>             | Contesto del prodotto.<br/>                      |
| [**ProductCode**](client-productcode.md)<br/>     | Prodotto client del componente in questione.<br/> |
| [**UserSID**](client-usersid.md)<br/>             | SID utente per il componente.<br/>                  |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 o versione successiva.<br/>                                         |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl> |
| IID<br/>     | IID \_ IClient è definito come 000C1098-0000-0000-C000-000000000046<br/>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso dell'interfaccia di automazione](using-the-automation-interface.md)
</dt> <dt>

[Esempi di script di Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




