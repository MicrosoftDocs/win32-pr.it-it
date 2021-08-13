---
description: Il metodo ClearSourceList dell'oggetto Installer rimuove tutte le origini di rete dall'elenco di origine.
ms.assetid: a4e4beb2-a4d7-48e7-9c8d-dd1ae19fe92a
title: Metodo Installer.ClearSourceList
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
ms.openlocfilehash: f16cc37556d217a217b814b5ce87cb705cd3105d4a8c2ad3f503d617aeda2cb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633039"
---
# <a name="installerclearsourcelist-method"></a>Metodo Installer.ClearSourceList

Il **metodo ClearSourceList** dell'oggetto [**Installer**](installer-object.md) rimuove tutte le origini di rete dall'elenco di origine.

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

Specifica il codice prodotto.

</dd> <dt>

*Utente* 
</dt> <dd>

Nome utente per l'installazione per utente; Stringa null o vuota per l'installazione per computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiSourceListClearAll**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearalla)
</dt> <dt>

[Resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 




