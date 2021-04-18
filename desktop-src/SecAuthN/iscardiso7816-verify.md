---
description: Costruisce un comando APDU (Application Protocol Data Unit) che avvia il confronto (nella scheda) dei dati di verifica inviati dal dispositivo di interfaccia con i dati di riferimento archiviati nella scheda (ad esempio, la password).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: 'Metodo ISCardISO7816:: Verify (scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardISO7816.Verify
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: c44bf65bfcebe6e76ce1ee955205b9c9163efcee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313736"
---
# <a name="iscardiso7816verify-method"></a>Metodo ISCardISO7816:: Verify

\[Il metodo **Verify** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Non è disponibile per l'utilizzo in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli Smart Card](/previous-versions/windows/desktop/secsmart/smart-card-modules) offrono funzionalità simili.\]

Il metodo **Verify** costruisce un comando APDU ( [*Application Protocol Data Unit*](../secgloss/a-gly.md) ) che avvia il confronto (nella scheda) dei dati di verifica inviati dal dispositivo di interfaccia con i dati di riferimento archiviati nella scheda (ad esempio, password).

## <a name="syntax"></a>Sintassi


```C++
HRESULT Verify(
  [in]      BYTE         byRefCtrl,
  [in]      LPBYTEBUFFER pData,
  [in, out] LPSCARDCMD   *ppCmd
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*byRefCtrl* \[ in\]
</dt> <dd>

Quantificatore dei dati di riferimento. Segue la codifica del controllo di riferimento P2.

Quando il corpo è vuoto, il comando può essere usato per recuperare il numero "X" di nuovi tentativi consentiti (SW1-SW2 = 63CX) o per verificare se la verifica non è necessaria (SW1-SW2 = 9000).



| Valore                                                                                                                                                                                    | Significato                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Nessuna informazione**</dt> </dl>                     | Posizione bit: 00000000<br/> P2 = 00 è riservata per indicare che non viene usato alcun qualificatore particolare nelle schede in cui il comando Verify fa riferimento ai dati del segreto in modo non ambiguo.<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Riferimento globale**</dt> </dl>         | Posizione bit: 0-------<br/> Un esempio di riferimento globale è costituito da una password.<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Riferimento specifico**</dt> </dl> | Posizione bit: 1-------<br/> Un esempio di riferimento specifico è la password specifica di DF.<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**RFU**</dt> </dl>                                                           | Posizione bit:-XX-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**Dati di riferimento \#**</dt> </dl>        | Posizione bit:---xxxxx<br/> Il numero di dati di riferimento può essere, ad esempio, un numero di password o un identificatore EF breve.<br/>                                                           |



 

</dd> <dt>

*pData* \[ in\]
</dt> <dd>

Puntatore ai dati di verifica. Questo parametro può essere **NULL**. Il valore predefinito è **NULL**.

</dd> <dt>

*ppCmd* \[ in uscita\]
</dt> <dd>

In input, un puntatore a un oggetto di interfaccia [**ISCardCmd**](iscardcmd.md) o **null**.

Al ritorno, viene compilato con il comando APDU creato da questa operazione. Se *ppCmd* è stato impostato su **null**, un oggetto [**ISCardCmd**](iscardcmd.md) della [*Smart Card*](../secgloss/s-gly.md) viene creato e restituito internamente utilizzando il puntatore *ppCmd* .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>          | Operazione riuscita.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato usato un parametro non valido.<br/> |
| <dl> <dt>**\_puntatore E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>            |
| <dl> <dt>**E \_ OutOfMemory**</dt> </dl> | Memoria insufficiente.<br/>                          |



 

## <a name="remarks"></a>Commenti

Lo stato di sicurezza può essere modificato in seguito a un confronto. I confronti non riusciti possono essere registrati nella scheda, ad esempio per limitare il numero di ulteriori tentativi di utilizzo dei dati di riferimento.

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

 

 
