---
description: Il metodo SourceListClearAll dell'oggetto Patch cancella l'elenco di origine completo di tutte le origini del tipo specificato per una patch. Accetta Type come parametro. Questo metodo chiama MsiSourceListClearAllEx.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Metodo Patch.SourceListClearAll
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ae7de8c0a830000b3100e84cacbf088fefb592ddaa912a7737a35ea009a3cfe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942301"
---
# <a name="patchsourcelistclearall-method"></a>Metodo Patch.SourceListClearAll

Il **metodo SourceListClearAll** dell'oggetto [**Patch**](patch-object.md) cancella l'elenco di origine completo di tutte le origini del tipo specificato per una patch. Accetta *Type* come parametro. Questo metodo chiama [**MsiSourceListClearAllEx.**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)

## <a name="syntax"></a>Sintassi


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Tipo* 
</dt> <dd>

Tipo di origine, ad esempio rete, URL o supporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Programma di installazione 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione 3.0 o versioni successive Windows Server 2003, Windows XP e Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IPatch IID è definito come \_ 000C10A1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[Non supportato in Windows Installer 2.0 e versioni precedenti](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




