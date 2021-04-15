---
title: Interrompi comando
description: Il comando break specifica una chiave per interrompere un comando che è stato richiamato usando il valore \ 0034; Wait \ 0034; bandiera. Questo comando è un comando di sistema MCI; viene interpretato direttamente da MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- comando Interrompi Windows Multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478934"
---
# <a name="break-command"></a>Interrompi comando

Il comando break specifica una chiave per interrompere un comando che è stato richiamato usando il flag "Wait". Questo comando è un comando di sistema MCI; viene interpretato direttamente da MCI.

Per inviare questo comando, chiamare la funzione [**mciSendString**](/previous-versions//dd757161(v=vs.85)) con il set di parametri *lpszCommand* come indicato di seguito.

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*
</dt> <dd>

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato quando il dispositivo viene aperto.

</dd> <dt>

<span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*
</dt> <dd>

Uno dei flag seguenti.



| Valore                 | Significato                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| nel *codice della chiave virtuale* | Specifica la chiave che interrompe un comando che è stato avviato utilizzando il flag "Wait". |
| spento                   | Disabilita la chiave di break corrente.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "Wait", "notify" o entrambi. Per i dispositivi digitali video e VCR è possibile specificare anche "test". Per ulteriori informazioni su questi flag, vedere [i flag Wait, Notify e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore.

## <a name="remarks"></a>Commenti

Quando il tasto Break è abilitato e l'utente preme il tasto identificato dal codice della chiave virtuale specificato nel parametro *lpszVirtKey* , il dispositivo restituisce il controllo all'applicazione. Se possibile, il comando continua l'esecuzione.

## <a name="examples"></a>Esempio

Il seguente comando imposta F2 come chiave di break per il dispositivo "audio".

``` syntax
break mysound on 113
```

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[MCI](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

