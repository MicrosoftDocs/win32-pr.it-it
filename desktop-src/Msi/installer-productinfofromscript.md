---
description: La proprietà ProductInfoFromScript dell'oggetto Installer restituisce il valore dell'attributo specificato archiviato in uno script di annuncio.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Programma di installazione::P proprietà roductInfoFromScript
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a4c8e29adb93f68228008770a95ad9fb9185e966
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332941"
---
# <a name="installerproductinfofromscript-property"></a>Programma di installazione::P proprietà roductInfoFromScript

La proprietà **ProductInfoFromScript** dell'oggetto [**Installer**](installer-object.md) restituisce il valore dell'attributo specificato archiviato in uno script di annuncio.

Questa proprietà è di sola scrittura.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a>Valore proprietà

## <a name="error-codes"></a>Codici di errore

Stringa o valore integer a seconda dell'attributo richiesto.

## <a name="remarks"></a>Commenti

La proprietà **ProductInfoFromScript** usa la funzione [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) .

## <a name="examples"></a>Esempio

Lo script di esempio seguente illustra l'uso della proprietà **ProductInfoFromScript** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
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

 

 




