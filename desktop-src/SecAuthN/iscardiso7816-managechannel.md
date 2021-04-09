---
description: Il metodo ManageChannel costruisce un comando APDU (Application Protocol Data Unit) che consente di aprire e chiudere i canali logici.
ms.assetid: a55b5b3f-0404-45bd-afeb-e96173319a50
title: 'Metodo ISCardISO7816:: ManageChannel (scardssp. h)'
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
ms.openlocfilehash: f0b9af92e280781405c2cb570c93e8873a279765
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049822"
---
# <a name="iscardiso7816managechannel-method"></a>Metodo ISCardISO7816:: ManageChannel

\[Il metodo **ManageChannel** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **ManageChannel** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che consente di aprire e chiudere i canali logici.

La funzione Open apre un nuovo canale logico diverso da quello di base. Sono disponibili opzioni per la scheda per assegnare un numero di canale logico o per il numero di canale logico da fornire alla scheda.

La funzione close chiude in modo esplicito un canale logico diverso da quello di base. Una volta completata la chiusura, il canale logico sarà disponibile per il riutilizzo.

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

*byChannelState* \[ in\]
</dt> <dd>

Bit B8 di P1 viene usato per indicare la funzione Open o la funzione close; Se B8 è 0, il canale di gestione deve aprire un canale logico e se B8 è 1, il canale di gestione deve chiudere un canale logico:

P1 = "00" da aprire

P1 = "80" da chiudere

Altri valori sono RFU

</dd> <dt>

*byChannel* \[ in\]
</dt> <dd>

Per la funzione Open (P1 = "00"), i bit B1 e B2 di P2 vengono usati per codificare il numero di canale logico nello stesso modo in cui si trova nella classe byte, mentre gli altri bit di P2 sono RFU.

Quando B1 e B2 di P2 sono **null**, la scheda assegnerà un numero di canale logico che verrà restituito in bits B1 e B2 del campo dati.

Quando B1 e/o B2 di P2 non sono **null**, codificano un numero di canale logico diverso da quello di base; la scheda apre quindi il numero di canale logico assegnato dall'esterno.

</dd> <dt>

*ppCmd* \[ in uscita\]
</dt> <dd>

In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.

Al ritorno, viene compilato con il comando APDU creato da questa operazione. Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione completata correttamente.<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Parametro non valido.<br/>                |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>      |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                    |



 

## <a name="remarks"></a>Commenti

Quando la funzione Open viene eseguita correttamente dal canale logico di base, MF deve essere selezionato in modo implicito come DF corrente e lo stato di sicurezza del nuovo canale logico deve essere lo stesso del canale logico di base dopo ATR. Lo stato di sicurezza del nuovo canale logico deve essere diverso da quello di qualsiasi altro canale logico.

Quando la funzione Open viene eseguita correttamente da un canale logico, che non è quello di base, il valore DF corrente del canale logico che ha emesso il comando verrà selezionato come DF corrente. Inoltre, lo stato di sicurezza per il nuovo canale logico deve corrispondere allo stato di sicurezza del canale logico da cui è stata eseguita la funzione di apertura.

Dopo una funzione di chiusura corretta, lo stato di sicurezza correlato a questo canale logico viene perso.

Per un elenco di tutti i metodi forniti da questa interfaccia, vedere [**ISCardISO7816**](iscardiso7816.md).

Oltre ai codici di errore COM elencati sopra, questa interfaccia può restituire un codice di errore della smart card se è stata chiamata una funzione Smart Card per completare la richiesta. Per ulteriori informazioni, vedere [valori restituiti della smart card](authentication-return-values.md).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop Windows XP\]<br/>                                             |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                    |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                   |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                          |
| Intestazione<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Libreria dei tipi<br/>             | <dl> <dt>Scardsrv. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardISO7816 è definito come 53B6AA68-3F56-11D0-916B-00AA00C18068<br/>        |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
