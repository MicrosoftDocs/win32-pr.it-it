---
description: Il metodo WriteBinary costruisce un comando APDU (Application Protocol Data Unit) che scrive valori binari in un file elementare.
ms.assetid: e38273d5-4eb0-4c0b-829a-c78e511a38bc
title: Metodo ISCardISO7816::WriteBinary (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.WriteBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 198a8eedc38636f60886af251c8520ef4726f362958c13a25fc3bf32653d7c52
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922920"
---
# <a name="iscardiso7816writebinary-method"></a>Metodo ISCardISO7816::WriteBinary

\[Il **metodo WriteBinary** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo WriteBinary** costruisce un comando APDU [*(Application Protocol Data Unit)*](../secgloss/a-gly.md) che scrive valori binari in un file elementare.

A seconda degli attributi del file, il comando esegue una delle operazioni seguenti:

-   OR logico dei bit già presenti nella scheda con i bit specificati nel comando APDU (lo stato logico dei bit del file è 0).
-   AND logico dei bit già presenti nella scheda con i bit specificati nel comando APDU (lo stato logico dei bit del file è 1).
-   La scrittura una sola volta nella scheda dei bit dati nel comando APDU.

Quando non viene specificata alcuna indicazione nel byte di codifica dei dati, viene applicato il comportamento OR logico.

## <a name="syntax"></a>Sintassi


```C++
HRESULT WriteBinary(
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

Offset nel percorso di scrittura dall'inizio del file binario (EF). Se b8=1 in P1, b7 e b6 di P1 sono impostati su zero (bit RFU), b5 a b1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da scrivere in unità dati dall'inizio del file. Se b8=0 in P1, P1 P2 è l'offset del primo byte da scrivere in unità dati \| \| dall'inizio del file.

</dd> <dt>

*byP2* \[ Pollici\]
</dt> <dd>

Offset nel percorso di scrittura dall'inizio del file binario (EF). Se b8=1 in P1, b7 e b6 di P1 sono impostati su zero (bit RFU), b5 a b1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da scrivere in unità dati dall'inizio del file. Se b8=0 in P1, P1 P2 è l'offset del primo byte da scrivere in unità dati \| \| dall'inizio del file.

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Puntatore alla stringa di unità dati da scrivere.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Nell'input, un puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

Al ritorno, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** [**smart card'oggetto ISCardCmd**](iscardcmd.md) viene creato internamente e restituito tramite il *puntatore ppCmd.* [](../secgloss/s-gly.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Il comando incapsulato può essere eseguito solo se lo stato di sicurezza del [*smart card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare in fase di elaborazione.

Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.

Quando un'operazione di scrittura binaria è stata applicata a un'unità dati di un EF di scrittura singola, qualsiasi altra operazione di scrittura che fa riferimento a questa unità dati verrà interrotta se il contenuto dell'unità dati o l'indicatore di stato di cancellazione logica (se presente) collegato a questa unità dati è diverso dallo stato di cancellazione logica.

Non è possibile scrivere file elementari senza una struttura trasparente. Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura trasparente.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816.**](iscardiso7816.md)

Oltre ai codici di errore COM elencati in precedenza, questa interfaccia può restituire un codice di errore smart card se è stata chiamata una funzione smart card per completare la richiesta. Per altre informazioni, vedere [Valori restituiti delle smart card.](authentication-return-values.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv.tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**ReadBinary**](iscardiso7816-readbinary.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> </dl>

 

 
