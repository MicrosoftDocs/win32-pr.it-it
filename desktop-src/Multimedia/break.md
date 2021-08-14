---
title: Comando break
description: Il comando break specifica una chiave per interrompere un comando richiamato usando \ 0034;wait \ 0034; Bandiera. Questo comando è un comando di sistema MCI. viene interpretato direttamente da MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- Comando break Windows Multimedia
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f99c8609b1364d374d91965816fde2d9c48b750d7bf0b3f6fb2957ed205a85a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375473"
---
# <a name="break-command"></a>Comando break

Il comando break specifica una chiave per interrompere un comando richiamato usando il flag "wait". Questo comando è un comando di sistema MCI. viene interpretato direttamente da MCI.

Per inviare questo comando, chiamare la [**funzione mciSendString**](/previous-versions//dd757161(v=vs.85)) con il parametro *lpszCommand* impostato come indicato di seguito.

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

Identificatore di un dispositivo MCI. Questo identificatore o alias viene assegnato all'apertura del dispositivo.

</dd> <dt>

<span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*
</dt> <dd>

Uno dei flag seguenti.



| Valore                 | Significato                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| sul *codice della chiave virtuale* | Specifica la chiave che interrompe un comando avviato usando il flag "wait". |
| spento                   | Disabilita la chiave di interruzione corrente.                                                 |



 

</dd> <dt>

<span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*
</dt> <dd>

Può essere "wait", "notify" o entrambi. Per i dispositivi digital-video e VCR, è anche possibile specificare "test". Per altre informazioni su questi flag, vedere [Flag di attesa, notifica e test](the-wait-notify-and-test-flags.md).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce zero in caso di esito positivo o un errore in caso contrario.

## <a name="remarks"></a>Commenti

Quando il tasto di interruzione è abilitato e l'utente preme il tasto identificato dal codice del tasto virtuale specificato nel *parametro lpszVirtKey,* il dispositivo restituisce il controllo all'applicazione. Se possibile, il comando continua l'esecuzione.

## <a name="examples"></a>Esempio

Il comando seguente imposta F2 come tasto di interruzione per il dispositivo "mysound".

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

[Mci](mci.md)
</dt> <dt>

[Stringhe di comando MCI](mci-command-strings.md)
</dt> </dl>

 

