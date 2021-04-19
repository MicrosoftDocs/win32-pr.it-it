---
description: La proprietà state restituisce lo stato di installazione di questa istanza della patch.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Proprietà patch. state
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.State
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f903ec66c2d55567fee9ccbc123e018e1dc7bacb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332017"
---
# <a name="patchstate-property"></a>Proprietà patch. state

La proprietà **state** restituisce lo stato di installazione di questa istanza della patch.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questa proprietà restituisce uno dei valori seguenti.



| Stato di installazione        | Significato                                                      |
|---------------------------|--------------------------------------------------------------|
| MSIPATCHSTATE \_ applicato    | La patch viene applicata a questa istanza del prodotto.                   |
| MSIPATCHSTATE \_ sostituito | La patch viene applicata a questa istanza del prodotto, ma viene sostituita. |
| MSIPATCHSTATE \_ obsoleto  | La patch viene applicata in questa istanza del prodotto ma è obsoleta.      |



 

Questo metodo può restituire \_ l'errore Unknown \_ patch, se l'oggetto [**patch**](patch-object.md) viene inizializzato con una stringa vuota per *ProductCode*.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 3,0 o versioni successive in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch è definito come 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Non supportato in Windows Installer 2,0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




