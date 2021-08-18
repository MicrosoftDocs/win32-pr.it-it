---
title: WINBIO_EVENT struttura (Winbio \_ types.h)
description: Contiene informazioni sullo stato inviate alla routine di callback quando viene generato un avviso di evento.
ms.assetid: f46df7ff-8197-49cb-b1f8-4e7e3288e3df
keywords:
- WINBIO_EVENT struttura Windows API Biometric Framework
- PWINBIO_EVENT puntatore alla struttura Windows'API Biometric Framework
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
ms.openlocfilehash: 6e3baab16ee7c3f825f317d7aa2c585cb4d8ae7d6d030b6f59a1555b95343015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118910544"
---
# <a name="winbio_event-structure"></a>Struttura WINBIO \_ EVENT

La **struttura \_ EVENT DI WINBIO** contiene informazioni sullo stato inviate alla routine di callback quando viene generato un avviso di evento.

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

<span id="WINBIO_EVENT_FP_UNCLAIMED"></span><span id="winbio_event_fp_unclaimed"></span>**WINBIO \_ EVENTO \_ FP \_ UNCLAIMED** (Il sensore ha rilevato uno scorrimento rapido del dito che non è stato richiesto dall'applicazione o dalla finestra che ha attualmente lo stato attivo. Il Windows Biometric Framework chiama la funzione di callback per indicare che si è verificato uno scorrimento rapido del dito ma non tenta di identificare l'impronta digitale.
</dt> <dt>

<span id="WINBIO_EVENT_FP_UNCLAIMED_IDENTIFY"></span><span id="winbio_event_fp_unclaimed_identify"></span>**WINBIO \_ EVENT \_ FP \_ UNCLAIMED \_ IDENTIFY** (IL sensore ha rilevato uno scorrimento rapido del dito che non è stato richiesto dall'applicazione o dalla finestra che ha attualmente lo stato attivo. Il Windows Biometric Framework tenta di identificare l'impronta digitale e passa il risultato di tale processo alla funzione di callback.
</dt> </dl> </dd> <dt>

**Parametri**
</dt> <dd> <dl> <dt>

**Unclaimed**
</dt> <dd>

Struttura restituita per l'acquisizione di campioni biometrici.

<dl> <dt>

**UnitId**
</dt> <dd>

Unità biometrica che ha generato il campione.

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valore **ULONG** che contiene informazioni aggiuntive relative alla mancata acquisizione di un campione biometrico. Se un'acquisizione ha esito positivo, questo parametro viene impostato su zero. Per l'acquisizione dell'impronta digitale vengono definiti i valori seguenti:

-   WINBIO \_ FP \_ TOO \_ HIGH
-   FP WINBIO \_ \_ TROPPO \_ BASSO
-   FP WINBIO \_ \_ TROPPO A \_ SINISTRA
-   FP WINBIO \_ \_ TROPPO A \_ DESTRA
-   WINBIO \_ FP \_ TOO \_ FAST
-   FP WINBIO \_ \_ TROPPO \_ LENTO
-   WINBIO \_ FP \_ POOR \_ QUALITY
-   WINBIO \_ FP \_ TOO \_ SKEWED
-   FP WINBIO \_ \_ TROPPO \_ BREVE
-   ERRORE DI UNIONE \_ FP WINBIO \_ \_

</dd> </dl> </dd> <dt>

**UnclaimedIdentify**
</dt> <dd>

Struttura restituita per l'acquisizione e l'identificazione biometrica. L'identificazione determina se un campione può essere associato a un modello biometrico esistente.

<dl> <dt>

**UnitId**
</dt> <dd>

Unità biometrica che ha generato il campione.

</dd> <dt>

**Identità**
</dt> <dd>

Struttura [**WINBIO \_ IDENTITY**](winbio-identity.md) che contiene il GUID o il SID dell'utente che fornisce l'esempio biometrico.

</dd> <dt>

**SubFactor**
</dt> <dd>

Valore [**\_ SUBTYPE BIOMETRIC \_ WINBIO**](winbio-biometric-subtype-constants.md) che specifica il fattore secondario associato a un campione biometrico. Il Windows Biometric Framework (WBF) supporta attualmente solo l'acquisizione di impronte digitali e usa le costanti seguenti per rappresentare le informazioni sui sottotipi.

-   WINBIO \_ ANSI \_ 381 \_ POS \_ UNKNOWN
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ RH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ THUMB
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ INDEX \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ MIDDLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ RING \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH \_ LITTLE \_ FINGER
-   WINBIO \_ ANSI \_ 381 \_ POS RH QUATTRO \_ \_ \_ DITA
-   WINBIO \_ ANSI \_ 381 \_ POS \_ LH QUATTRO \_ \_ DITA
-   WINBIO \_ ANSI \_ 381 \_ POS \_ TWO \_ THUMBS

> [!IMPORTANT]
>
> Non tentare di convalidare il valore fornito per il *valore SubFactor.* Il Windows biometrica convalida il valore fornito prima di passarlo all'implementazione. Se il valore è **WINBIO \_ SUBTYPE \_ NO INFORMATION \_ o** **WINBIO \_ SUBTYPE \_ ANY,** convalidare dove appropriato.

 

</dd> <dt>

**RejectDetail**
</dt> <dd>

Valore **ULONG** che contiene informazioni aggiuntive sull'errore di acquisizione di un campione biometrico. Se l'acquisizione ha esito positivo, questo parametro è impostato su zero. Per l'acquisizione dell'impronta digitale vengono definiti i valori seguenti:

-   WINBIO \_ FP \_ TOO \_ HIGH
-   FP WINBIO \_ \_ TROPPO \_ BASSO
-   FP WINBIO \_ \_ TROPPO A \_ SINISTRA
-   FP WINBIO \_ \_ TROPPO A \_ DESTRA
-   WINBIO \_ FP \_ TOO \_ FAST
-   FP WINBIO \_ \_ TROPPO \_ LENTO
-   WINBIO \_ FP \_ POOR \_ QUALITY
-   WINBIO \_ FP \_ TOO \_ SKEWED
-   FP WINBIO \_ \_ TROPPO \_ BREVE
-   ERRORE DI UNIONE \_ FP WINBIO \_ \_

</dd> </dl> </dd> <dt>

**Error (Errore) (Error (Errore)e)**
</dt> <dd>

Struttura che identifica l'esito positivo o negativo dell'operazione monitorata.

<dl> <dt>

**ErrorCode**
</dt> <dd>

**Valore HRESULT** che contiene S OK o un codice di errore generato dai calcoli eseguiti da \_ Windows Biometric Framework.

</dd> </dl> </dd> </dl> </dd> </dl>

## <a name="remarks"></a>Commenti

Chiamare la [**funzione WinBioRegisterEventMonitor per**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor) registrare una routine di callback per ricevere notifiche degli eventi Windows Biometric Framework. Il callback è una funzione personalizzata che è necessario definire per l'applicazione.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                                                    |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Winbio \_ types.h (include Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture delle applicazioni client](client-application-structures.md)
</dt> <dt>

[**WinBioRegisterEventMonitor**](/windows/desktop/api/Winbio/nf-winbio-winbioregistereventmonitor)
</dt> </dl>

 

 





