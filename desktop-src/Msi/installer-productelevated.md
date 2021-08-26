---
description: La proprietà ProductElevated dell'oggetto Installer restituisce True se il prodotto è gestito o False se il prodotto non è gestito.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Proprietà Installer::P roductElevated
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 515964481c62e4588f3d9b75d168bffd2876cb22ce526e8ec0eaa41e226c110e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129391"
---
# <a name="installerproductelevated-property"></a>Proprietà Installer::P roductElevated

La **proprietà ProductElevated** dell'oggetto [**Installer**](installer-object.md) restituisce True se il prodotto è gestito o False se il prodotto non è gestito.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Valore proprietà

GUID del codice prodotto completo del prodotto. Questo parametro è obbligatorio.

## <a name="remarks"></a>Commenti

La **proprietà ProductElevated** usa la [**funzione MsiIsProductElevated.**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) La restituzione della proprietà non prende in considerazione i [criteri AlwaysInstallElevated.](alwaysinstallelevated.md)

## <a name="examples"></a>Esempio

Lo script di esempio seguente illustra l'uso **della proprietà ProductElevated** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 4.5 in Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Programma di installazione**](installer-object.md)
</dt> <dt>

[Non supportato in Windows Installer 3.1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




