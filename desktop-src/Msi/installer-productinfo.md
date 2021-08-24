---
description: La proprietà ProductInfo è una proprietà di sola lettura che restituisce il valore dell'attributo specificato per un prodotto installato o pubblicato.
ms.assetid: 144cbba7-ec2b-44cd-acc8-868c210ccebd
title: Proprietà Installer.ProductInfo (Oemupgex.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 5d04ad49fd8c1cf017131b5ded6be088e6436731b6bd97dd437060d09988d3aa
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119745291"
---
# <a name="installerproductinfo-property"></a>Proprietà Installer.ProductInfo

La **proprietà ProductInfo** è una proprietà di sola lettura che restituisce il valore dell'attributo specificato per un prodotto installato o pubblicato.

Questa proprietà è di sola lettura.

## <a name="syntax"></a>Sintassi


```JScript
propVal = Installer.ProductInfo
```



## <a name="property-value"></a>Valore proprietà

## <a name="remarks"></a>Commenti

La **proprietà ProductInfo** ("LocalPackage") non restituisce necessariamente un percorso al pacchetto memorizzato nella cache. Le installazioni in modalità manutenzione non devono essere richiamate da LocalPackage. Il pacchetto memorizzato nella cache è solo per usi interni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versione successiva Windows Server 2003 o Windows XP.<br/> |
| Intestazione<br/>  | <dl> <dt>Oemupgex.h</dt> </dl>                                                                                                                                                                                 |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID IInstaller è definito come \_ 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiGetProductInfo**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoa)
</dt> <dt>

[**MsiGetUserInfo**](/windows/desktop/api/Msi/nf-msi-msigetuserinfoa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




