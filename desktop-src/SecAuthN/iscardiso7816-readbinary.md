---
description: Il metodo ReadBinary costruisce un comando APDU (Application Protocol Data Unit) che acquisisce un messaggio di risposta che fornisce tale parte del contenuto di un file elementare con struttura trasparente.
ms.assetid: 15394c21-1e07-4ea1-8f11-817e07b31f9b
title: 'Metodo ISCardISO7816:: ReadBinary (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.ReadBinary
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: a29093d8725a3390df9837f4e2f395cfcf2eef29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103884490"
---
# <a name="iscardiso7816readbinary-method"></a>Metodo ISCardISO7816:: ReadBinary

\[Il metodo **ReadBinary** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **ReadBinary** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che acquisisce un messaggio di risposta che fornisce tale parte del contenuto di un file elementare con struttura trasparente.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ReadBinary(
  [in]      BYTE       byP1,
  [in]      BYTE       byP2,
  [in]      LONG       lBytesToRead,
  [in, out] LPSCARDCMD *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byP1* \[ in\]
</dt> <dd>

Il campo P1-P2, offset al primo byte da leggere dall'inizio del file. Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da leggere in unità dati dall'inizio del file. Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da leggere nelle unità dati dall'inizio del file.

</dd> <dt>

*byP2* \[ in\]
</dt> <dd>

Il campo P1-P2, offset al primo byte da leggere dall'inizio del file. Se B8 = 1 in P1, B7 e B6 di P1 sono impostati su zero (RFU bit), B5 a B1 di P1 sono un identificatore EF breve e P2 è l'offset del primo byte da leggere in unità dati dall'inizio del file. Se B8 = 0 in P1, P1 \| \| P2 è l'offset del primo byte da leggere nelle unità dati dall'inizio del file.

</dd> <dt>

*lBytesToRead* \[ in\]
</dt> <dd>

Numero di byte da leggere dall'EF trasparente.

Se il campo le contiene solo zeri, entro il limite di 256 per la lunghezza breve o 65536 per la lunghezza estesa, tutti i byte fino alla fine del file devono essere letti.

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

Il comando incapsulato può essere eseguito solo se lo stato di sicurezza della [*Smart Card*](../secgloss/s-gly.md) soddisfa gli attributi di sicurezza del file elementare elaborato.

Quando il comando contiene un identificatore elementare breve valido, imposta il file come file elementare corrente.

Non è possibile cancellare i file elementari senza una struttura trasparente. Il comando incapsulato viene interrotto se applicato a un file elementare senza una struttura trasparente.

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

[**EraseBinary**](iscardiso7816-erasebinary.md)
</dt> <dt>

[**ISCardISO7816**](iscardiso7816.md)
</dt> <dt>

[**UpdateBinary**](iscardiso7816-updatebinary.md)
</dt> <dt>

[**WriteBinary**](iscardiso7816-writebinary.md)
</dt> </dl>

 

 
