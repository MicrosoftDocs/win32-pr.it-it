---
description: Costruisce un comando APDU (Application Protocol Data Unit) che imposta in sequenza parte del contenuto di un file elementare sullo stato logico cancellato, a partire da un offset specificato.
ms.assetid: 89e2371e-e27d-475b-9427-bbf6d614c473
title: Metodo ISCardISO7816::EraseBinary (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.EraseBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 012927e21e3ed897136a9b058ae03539b7d2e2ac0e581d04cb14235aed9ae80f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119007899"
---
# <a name="iscardiso7816erasebinary-method"></a>Metodo ISCardISO7816::EraseBinary

\[Il **metodo EraseBinary** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo EraseBinary** costruisce un comando APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) che imposta in sequenza parte del contenuto di un file elementare sullo stato logico cancellato, a partire da un offset specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT EraseBinary(
  [in]      BYTE         byP1,
  [in]      BYTE         byP2,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byP1* \[ Pollici\]
</dt> <dd>

Posizione RFU.

Se b8=1 in P1, b7 e b6 di P1 sono impostati su zero (bit RFU), da b5 a b1 di P1 è un identificatore EF breve e P2 è l'offset del primo byte da cancellare (in unità di dati) dall'inizio del file.

Se b8=0 in P1, P1 P2 è l'offset del primo byte da cancellare (in unità dati) dall'inizio \| \| del file.

Se il campo dati è presente, indica l'offset della prima unità dati da non cancellare. Questo offset deve essere maggiore di quello codificato in P1-P2. Quando il campo dati è vuoto, il comando cancella fino alla fine del file.

</dd> <dt>

*byP2* \[ Pollici\]
</dt> <dd>

Posizione RFU.

Se b8=1 in P1, b7 e b6 di P1 sono impostati su zero (bit RFU), da b5 a b1 di P1 è un identificatore EF breve e P2 è l'offset del primo byte da cancellare (in unità di dati) dall'inizio del file.

Se b8=0 in P1, P1 P2 è l'offset del primo byte da cancellare (in unità dati) dall'inizio \| \| del file.

Se il campo dati è presente, indica l'offset della prima unità dati da non cancellare. Questo offset deve essere maggiore di quello codificato in P1-P2. Quando il campo dati è vuoto, il comando cancella fino alla fine del file.

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Puntatore ai dati che specifica l'intervallo di cancellazione. Questo parametro può essere **NULL.**

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

In input, puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

In caso di restituzione, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** un [*smart card*](../secgloss/s-gly.md) [**isCardCmd viene**](iscardcmd.md) creato internamente e restituito usando il *puntatore ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato passato un parametro non valido.<br/> |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido.<br/>              |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                            |



 

## <a name="remarks"></a>Commenti

Il comando incapsulato può essere eseguito solo se lo stato di sicurezza del [*smart card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare in fase di elaborazione.

Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.

I file elementari senza una struttura trasparente non possono essere cancellati. Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura trasparente.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un smart card di errore se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Smart Card Return Values](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
