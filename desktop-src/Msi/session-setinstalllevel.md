---
description: Il metodo SetInstallLevel dell'oggetto Session imposta il livello di installazione per l'installazione corrente su un valore specificato e Ricalcola gli Stati Select e installato per tutte le funzionalità nella tabella Feature.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Session. SetInstallLevel, metodo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333036"
---
# <a name="sessionsetinstalllevel-method"></a>Session. SetInstallLevel, metodo

Il metodo **SetInstallLevel** dell'oggetto [**Session**](session-object.md) imposta il livello di installazione per l'installazione corrente su un valore specificato e Ricalcola gli Stati Select e installato per tutte le funzionalità nella tabella Feature. Imposta inoltre lo stato dell'azione di ogni componente nella [tabella dei componenti](component-table.md) in base al nuovo livello.

## <a name="syntax"></a>Sintassi


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*installLevel* 
</dt> <dd>

Richiesto nuovo livello di installazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Prima di chiamare **SetInstallLevel** è necessario eseguire l' [azione CostInitialize](costinitialize-action.md) .

Se viene passato 0 per il parametro *installLevel* , il livello di installazione corrente non viene modificato, ma tutte le funzionalità sono ancora aggiornate in base al livello di installazione corrente. Questa funzionalità, ad esempio, può essere usata dal modulo handler per reimpostare tutte le selezioni sui rispettivi stati predefiniti iniziali in qualsiasi punto del processo di selezione dell'interfaccia utente.

Se il metodo ha esito negativo, è possibile ottenere informazioni estese sull'errore usando il metodo [**LastErrorRecord**](installer-lasterrorrecord.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versione<br/> | Windows Installer 5,0 in Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 in Windows Server 2008 o Windows Vista. Windows Installer in Windows Server 2003 o Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISession è definito come 000C109E-0000-0000-C000-000000000046<br/>                                                                                                                                                                             |



 

 




