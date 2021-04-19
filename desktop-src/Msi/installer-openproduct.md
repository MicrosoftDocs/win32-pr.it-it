---
description: Il metodo OpenProduct dell'oggetto Installer apre un pacchetto di installazione per un prodotto installato utilizzando il codice prodotto e restituisce un oggetto sessione.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Installer. OpenProduct, metodo
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
ms.openlocfilehash: 9fd25a1f204a6d42cd4cb6e330d7d69da2cddb07
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332178"
---
# <a name="installeropenproduct-method"></a>Installer. OpenProduct, metodo

Il metodo **OpenProduct** dell'oggetto [**Installer**](installer-object.md) apre un pacchetto di installazione per un prodotto installato utilizzando il codice prodotto e restituisce un oggetto [**sessione**](session-object.md) .

## <a name="syntax"></a>Sintassi


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*productCode* 
</dt> <dd>

Stringa obbligatoria che contiene il codice prodotto univoco ( [GUID](guid.md)) o un descrittore di attivazione scritto dal programma di installazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Si noti che solo un oggetto [**sessione**](session-object.md) può essere aperto da un singolo processo. Non è possibile usare **OpenProduct** in un'azione personalizzata perché l'installazione attiva è l'unica sessione consentita.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller è definito come 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




