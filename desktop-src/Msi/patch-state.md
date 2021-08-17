---
description: La proprietà State restituisce lo stato di installazione di questa istanza della patch.
ms.assetid: b01b2839-d867-4353-99d0-8c612cd1eb0c
title: Patch.State - proprietà
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
ms.openlocfilehash: b28eee03cfc74537c8be7669124a4f70db40ca88196678889553978232c934c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942291"
---
# <a name="patchstate-property"></a>Patch.State - proprietà

La **proprietà State** restituisce lo stato di installazione di questa istanza della patch.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Patch.State
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

Questa proprietà restituisce uno dei valori seguenti.



| Stato dell'installazione        | Significato                                                      |
|---------------------------|--------------------------------------------------------------|
| MSIPATCHSTATE \_ APPLICATO    | La patch viene applicata a questa istanza del prodotto.                   |
| MSIPATCHSTATE \_ SOSTITUITO | La patch viene applicata a questa istanza del prodotto, ma viene sostituita. |
| MSIPATCHSTATE \_ OBSOLETO  | Patch viene applicata in questa istanza del prodotto, ma obsoleta.      |



 

Questo metodo può restituire ERROR \_ UNKNOWN \_ PATCH, se [**l'oggetto Patch**](patch-object.md) viene inizializzato con una stringa vuota per *ProductCode.*

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva in Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch è definito come 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiGetPatchInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetpatchinfoexa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




