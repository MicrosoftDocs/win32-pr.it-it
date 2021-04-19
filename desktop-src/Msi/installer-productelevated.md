---
description: La proprietà ProductElevated dell'oggetto Installer restituisce true se il prodotto è gestito o false se il prodotto non è gestito.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Programma di installazione::P proprietà roductElevated
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
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332947"
---
# <a name="installerproductelevated-property"></a>Programma di installazione::P proprietà roductElevated

La proprietà **ProductElevated** dell'oggetto [**Installer**](installer-object.md) restituisce true se il prodotto è gestito o false se il prodotto non è gestito.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Valore proprietà

GUID completo del codice prodotto del prodotto. Questo parametro è obbligatorio.

## <a name="remarks"></a>Commenti

La proprietà **ProductElevated** usa la funzione [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) . Il ritorno della proprietà non prende in considerazione il criterio [AlwaysInstallElevated](alwaysinstallelevated.md) .

## <a name="examples"></a>Esempio

Lo script di esempio seguente illustra l'uso della proprietà **ProductElevated** .


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
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer 4,5 in Windows Server 2003 e Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Programma di installazione**](installer-object.md)
</dt> <dt>

[Non supportato in Windows Installer 3,1 e versioni precedenti](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




