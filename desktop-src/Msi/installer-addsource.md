---
description: Il metodo AddSource dell'oggetto Installer aggiunge un'origine all'elenco di origini di rete valide nell'elenco di origine.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Installer. AddSource, metodo
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
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328066"
---
# <a name="installeraddsource-method"></a>Installer. AddSource, metodo

Il metodo **addsource** dell'oggetto [**Installer**](installer-object.md) aggiunge un'origine all'elenco di origini di rete valide nell'elenco di origine.

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

Specifica il codice del prodotto.

</dd> <dt>

*Utente* 
</dt> <dd>

Nome utente per l'installazione per utente; stringa null o vuota per l'installazione per computer.

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
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**MsiSourceListAddSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[resilienza di origine](source-resiliency.md)
</dt> </dl>

 

 




