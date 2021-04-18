---
description: La proprietà ComponentRequestState dell'oggetto Session Ottiene o richiede una modifica nello stato dell'azione di una riga nella tabella dei componenti.
ms.assetid: d0b50c25-dca6-4bdf-8ee9-490e436fcc5b
title: Proprietà Session. ComponentRequestState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentRequestState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 17ec77c5498a808e0d7ac0f2881057979d7db0c4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106329110"
---
# <a name="sessioncomponentrequeststate-property"></a>Proprietà Session. ComponentRequestState

La proprietà **ComponentRequestState** dell'oggetto [**Session**](session-object.md) Ottiene o richiede una modifica nello stato dell'azione di una riga nella [tabella dei componenti](component-table.md).

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Session.ComponentRequestState
```



## <a name="property-value"></a>Valore proprietà

Nome stringa obbligatorio dell'elemento componente, chiave primaria della tabella dei componenti.

## <a name="remarks"></a>Commenti



| Stato selezione        | Valore | Descrizione                                                    |
|------------------------|-------|----------------------------------------------------------------|
| Null                   | Null  | Richiede che non venga eseguita alcuna azione per questo elemento.                |
| msiInstallStateAbsent  | 2     | L'elemento deve essere rimosso.                                         |
| msiInstallStateLocal   | 3     | L'elemento deve essere installato localmente.                               |
| msiInstallStateSource  | 4     | L'elemento deve essere installato ed eseguito dal supporto di origine.         |
| msiInstallStateDefault | 5     | Se installato, l'elemento deve essere reinstallato nello stesso stato. |



 

Se la proprietà ha esito negativo, è possibile ottenere informazioni estese sugli errori usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




