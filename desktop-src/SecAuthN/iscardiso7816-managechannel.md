---
description: Il metodo ManageChannel costruisce un comando APDU (Application Protocol Data Unit) che apre e chiude i canali logici.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: Metodo ISCardISO7816::ManageChannel (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ManageChannel
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 92fb91c0630996938e247dbc244ac0c311c52531401367d5326bd197ffaabf9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481121"
---
# <a name="iscardiso7816managechannel-method"></a>Metodo ISCardISO7816::ManageChannel

\[Il **metodo ManageChannel** è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il **metodo ManageChannel** costruisce un [*comando APDU (Application Protocol Data Unit)*](../secgloss/a-gly.md) che apre e chiude i canali logici.

La funzione open apre un nuovo canale logico diverso da quello di base. Vengono fornite opzioni per la scheda per assegnare un numero di canale logico o per il numero di canale logico da assegnare alla scheda.

La funzione close chiude in modo esplicito un canale logico diverso da quello di base. Dopo la chiusura corretta, il canale logico sarà disponibile per il nuovo utilizzo.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ManageChannel(
  [in]      BYTE       byChannelState,
  [in]      BYTE       byChannel,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byChannelState* \[ Pollici\]
</dt> <dd>

Il bit b8 di P1 viene usato per indicare la funzione open o la funzione close. se b8 è 0, MANAGE CHANNEL deve aprire un canale logico e se b8 è 1, MANAGE CHANNEL chiuderà un canale logico:

P1 = '00' da aprire

P1 = '80' da chiudere

Altri valori sono RFU

</dd> <dt>

*byChannel* \[ Pollici\]
</dt> <dd>

Per la funzione open (P1 = '00'), i bit b1 e b2 di P2 vengono usati per codificare il numero di canale logico nello stesso modo in cui nel byte della classe, gli altri bit di P2 sono RFU.

Quando b1 e b2 di P2 sono **NULL,** la scheda assegna un numero di canale logico che verrà restituito nei bit b1 e b2 del campo dati.

Quando b1 e/o b2 di P2 non sono **NULL,** codificano un numero di canale logico diverso da quello di base. quindi la scheda aprirà il numero di canale logico assegnato esternamente.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

In input, puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

In caso di restituzione, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** un [*smart card*](../secgloss/s-gly.md) [**isCardCmd viene**](iscardcmd.md) creato internamente e restituito usando il *puntatore ppCmd.*

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**PUNTATORE E \_**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Quando la funzione open viene eseguita correttamente dal canale logico di base, l'MF deve essere selezionato in modo implicito come DF corrente e lo stato di sicurezza del nuovo canale logico deve essere lo stesso del canale logico di base dopo ATR. Lo stato di sicurezza del nuovo canale logico deve essere separato da quello di qualsiasi altro canale logico.

Quando la funzione open viene eseguita correttamente da un canale logico, che non è quello di base, il valore DF corrente del canale logico che ha eseguito il comando verrà selezionato come DF corrente. Inoltre, lo stato di sicurezza per il nuovo canale logico deve essere uguale allo stato di sicurezza del canale logico da cui è stata eseguita la funzione aperta.

Dopo una corretta chiusura della funzione, lo stato di sicurezza correlato a questo canale logico viene perso.

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
</dt> </dl>

 

 
