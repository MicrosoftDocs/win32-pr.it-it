---
description: Il metodo OpenProduct dell'oggetto Installer apre un pacchetto di installazione per un prodotto installato usando il codice prodotto e restituisce un oggetto Session.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Metodo Installer.OpenProduct
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3aa6176b297261968a63b2f723a65ea14b45b8d3628b200be92df556adc5c2b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129381"
---
# <a name="installeropenproduct-method"></a>Metodo Installer.OpenProduct

Il **metodo OpenProduct** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto di installazione per un prodotto installato usando il codice prodotto e restituisce un [**oggetto Session.**](session-object.md)

## <a name="syntax"></a>Sintassi


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Productcode* 
</dt> <dd>

Stringa obbligatoria contenente il codice prodotto univoco [(GUID](guid.md)) o un descrittore di attivazione scritto dal programma di installazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Si noti che un [**solo oggetto Session**](session-object.md) può essere aperto da un singolo processo. **OpenProduct non** può essere usato in un'azione personalizzata perché l'installazione attiva è l'unica sessione consentita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Programma di installazione 5.0 Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4.0 o Windows Installer 4.5 in Windows Server 2008 o Windows Vista. Windows Programma di installazione Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




