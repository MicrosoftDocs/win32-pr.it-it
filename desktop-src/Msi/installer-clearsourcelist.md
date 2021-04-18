---
description: Il metodo ClearSourceList dell'oggetto Installer rimuove tutte le origini di rete dall'elenco di origine.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Installer. ClearSourceList, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ClearSourceList
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f9468775c75533b766a160a390410908d04bf6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326985"
---
# <a name="installerclearsourcelist-method"></a>Installer. ClearSourceList, metodo

Il metodo **ClearSourceList** dell'oggetto [**Installer**](installer-object.md) rimuove tutte le origini di rete dall'elenco di origine.

## <a name="syntax"></a>Sintassi


```JScript
Installer.ClearSourceList(
  Product,
  User
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Prodotto* 
</dt> <dd>

Specifica il codice del prodotto.

</dd> <dt>

*Utente* 
</dt> <dd>

Nome utente per l'installazione per utente; stringa null o vuota per l'installazione per computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 




