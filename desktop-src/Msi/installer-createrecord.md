---
description: Il metodo CreaRecord dell'oggetto Installer restituisce un nuovo oggetto record con il numero di campi richiesto.
ms.assetid: 7f9adb28-87da-48dd-ab5c-e138b356b133
title: Installer. CreaRecord, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CreateRecord
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8095e35a7e424a50448f1f0d948b9224bcdaa423
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333877"
---
# <a name="installercreaterecord-method"></a>Installer. CreaRecord, metodo

Il metodo **CreaRecord** dell'oggetto [**Installer**](installer-object.md) restituisce un nuovo oggetto [**record**](record-object.md) con il numero di campi richiesto.

## <a name="syntax"></a>Sintassi


```JScript
Installer.CreateRecord(
  count
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*count* 
</dt> <dd>

Numero di campi obbligatorio, che può essere 0. Il numero massimo di campi in un record è limitato a 65535.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Il campo 0, non uno dei campi in *count*, viene in genere usato per gli elementi orientati ai record, ad esempio le stringhe di formato o i codici op di esecuzione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




