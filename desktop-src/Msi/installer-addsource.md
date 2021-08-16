---
description: Il metodo AddSource dell'oggetto Installer aggiunge un'origine all'elenco di origini di rete valide nell'elenco sourcelist.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Metodo Installer.AddSource
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8c5e2b87a1fc9a660ae835d9fb1cfa465673bb6698144a9695cbfb264535a948
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118633165"
---
# <a name="installeraddsource-method"></a>Metodo Installer.AddSource

Il **metodo AddSource** dell'oggetto [**Installer**](installer-object.md) aggiunge un'origine all'elenco di origini di rete valide nell'elenco sourcelist.

## <a name="syntax"></a>Sintassi


```JScript
Installer.AddSource(
  Product,
  User,
  Source
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

</dd> <dt>

*Origine* 
</dt> <dd>

Puntatore alla stringa che specifica l'origine.

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

[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 




