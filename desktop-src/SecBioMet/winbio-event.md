---
title: Struttura WINBIO_EVENT ( \_ tipi WINBIO. h)
description: Contiene informazioni sullo stato inviate alla routine di callback quando viene generata una notifica di evento.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- Struttura di WINBIO_EVENT Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_EVENT
topic_type:
- apiref
api_name:
- WINBIO_EVENT
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75b6a8301ea5dab7d860e5bd7fb32c69277bad63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302344"
---
# <a name="winbio_event-structure"></a>\_Struttura dell'evento WINBIO

La struttura dell' **\_ evento WINBIO** contiene le informazioni sullo stato inviate alla routine di callback quando viene generata una notifica di evento.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _WINBIO_EVENT {
  WINBIO_EVENT_TYPE Type;
  union {
    struct {
      WINBIO_UNIT_ID       UnitId;
      WINBIO_REJECT_DETAIL RejectDetail;
    } Unclaimed;
    struct {
      WINBIO_UNIT_ID           UnitId;
      WINBIO_IDENTITY          Identity;
      WINBIO_BIOMETRIC_SUBTYPE SubFactor;
      WINBIO_REJECT_DETAIL     RejectDetail;
    } UnclaimedIdentify;
    struct {
      HRESULT ErrorCode;
    } Error;
  } Parameters;
} WINBIO_EVENT, *PWINBIO_EVENT;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Valore che specifica il tipo di avviso di evento del provider di servizi generato. L'unico provider attualmente supportato è il sensore di impronta digitale. Questo sensore supporta i flag seguenti.

<dl> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENTO \_ FP non \_ recuperato** (il sensore ha rilevato una swipe del dito non richiesto dall'applicazione o dalla finestra che attualmente ha lo stato attivo. Il Windows Biometric Framework chiama la funzione di callback per indicare che si è verificato un dito sfiorato ma non tenta di identificare l'impronta digitale.
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ EVENTO \_ FP senza \_ attestazione \_** (il sensore ha rilevato una striscia di dita non richiesta dall'applicazione o dalla finestra che attualmente ha lo stato attivo. Il Windows Biometric Framework tenta di identificare l'impronta digitale e passa il risultato di tale processo alla funzione di callback.
</dt> </dl> </dd> <dt>

**Parametri**
</dt> <dd> <dl> <dt>

**Richiesti**
</dt> <dd>

Struttura restituita per l'acquisizione di esempio biometrica.

<dl> <dt>

**UnitId**
</dt> <dd>

Unità biometrica che ha generato l'esempio.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valore **ULONG** che contiene informazioni aggiuntive sull'errore di acquisizione di un campione biometrico. Se un'acquisizione ha avuto esito positivo, questo parametro è impostato su zero. Per l'acquisizione di impronte digitali vengono definiti i valori seguenti:

-   WINBIO \_ FP \_ troppo \_ alta
-   WINBIO \_ FP \_ troppo \_ basso
-   WINBIO \_ FP \_ troppo a \_ sinistra
-   WINBIO \_ FP \_ troppo a \_ destra
-   WINBIO \_ FP \_ troppo \_ veloce
-   WINBIO \_ FP \_ troppo \_ lento
-   WINBIO \_ FP \_ scarsa \_ qualità
-   WINBIO \_ FP \_ troppo \_ sbilanciato
-   WINBIO \_ FP \_ troppo \_ breve
-   \_errore di \_ merge WINBIO FP \_

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

Struttura restituita per l'acquisizione e l'identificazione biometriche. L'identificazione determina se un campione può essere associato a un modello biometrico esistente.

<dl> <dt>

**UnitId**
</dt> <dd>

Unità biometrica che ha generato l'esempio.

</dd> <dt>

**Identità**
</dt> <dd>

Struttura [**di \_ identità WINBIO**](winbio-identity.md) che contiene il GUID o il SID dell'utente che fornisce l'esempio biometrico.

</dd> <dt>

**Sottofattore**
</dt> <dd>

Valore [**del \_ \_ SOTTOtipo biometrico WINBIO**](winbio-biometric-subtype-constants.md) che specifica il Sottofattore associato a un campione biometrico. Il Windows Biometric Framework (WBF) supporta attualmente solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sui sottotipi.

-   WINBIO \_ ANSI \_ 381 \_ POS \_ sconosciuta
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ pollice RH
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ - \_ dito indice
-   WINBIO \_ ANSI \_ 381 \_ POS \_ \_ secondo \_ dito medio
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ \_ anulare
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ piccolo \_ dito
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Thumb
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito indice LH \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ dito medio SX \_
-   WINBIO \_ ANSI \_ 381 \_ POS \_ - \_ \_ dito sinistro
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ Little \_ Finger
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ quattro \_ dita
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ quattro \_ dita
-   WINBIO \_ ANSI \_ 381 \_ POS \_ due \_ pollici

> [!IMPORTANT]
>
> Non tentare di convalidare il valore specificato per il valore del *Sottofattore* . Il servizio biometria di Windows convaliderà il valore fornito prima di passarlo all'implementazione. Se il valore è **WINBIO, non vi sono \_ \_ \_ informazioni** o **\_ sottotipi \_ di WINBIO**, quindi eseguire la convalida laddove appropriato.

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valore **ULONG** che contiene informazioni aggiuntive sull'errore di acquisizione di un campione biometrico. Se l'acquisizione ha avuto esito positivo, questo parametro è impostato su zero. Per l'acquisizione di impronte digitali vengono definiti i valori seguenti:

-   WINBIO \_ FP \_ troppo \_ alta
-   WINBIO \_ FP \_ troppo \_ basso
-   WINBIO \_ FP \_ troppo a \_ sinistra
-   WINBIO \_ FP \_ troppo a \_ destra
-   WINBIO \_ FP \_ troppo \_ veloce
-   WINBIO \_ FP \_ troppo \_ lento
-   WINBIO \_ FP \_ scarsa \_ qualità
-   WINBIO \_ FP \_ troppo \_ sbilanciato
-   WINBIO \_ FP \_ troppo \_ breve
-   \_errore di \_ merge WINBIO FP \_

</dd> </dl> </dd> <dt>

**Error (Errore) (Error (Errore)e)**
</dt> <dd>

Struttura che identifica l'esito positivo o negativo dell'operazione sottoposta a monitoraggio.

<dl> <dt>

**ErrorCode**
</dt> <dd>

Valore **HRESULT** che contiene S \_ OK o un codice di errore risultante da calcoli eseguiti dal Windows Biometric Framework.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Chiamare la funzione [**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) per registrare una routine di callback per ricevere notifiche degli eventi dal Windows Biometric Framework. Il callback è una funzione personalizzata che è necessario definire per l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                                    |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>\_Tipi WinBio. h (includere WinBio. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





