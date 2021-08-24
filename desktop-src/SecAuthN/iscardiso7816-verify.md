---
description: Costruisce un comando APDU (Application Protocol Data Unit) che avvia il confronto (nella scheda) dei dati di verifica inviati dal dispositivo di interfaccia con i dati di riferimento archiviati nella scheda (ad esempio, la password).
ms.assetid: a0837c39-d741-42eb-88b2-87c4e043e64f
title: Metodo ISCardISO7816::Verify (Scardssp.h)
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
ms.openlocfilehash: f0d01fe47133ddeaf7bba32a91711d76783bdfbb0a28762d7ddb7f9054d0108d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014441"
---
# <a name="iscardiso7816verify-method"></a>Metodo ISCardISO7816::Verify

\[Il **metodo** Verify è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Non è disponibile per l'uso in Windows Server 2003 con Service Pack 1 (SP1) e versioni successive, Windows Vista, Windows Server 2008 e versioni successive del sistema operativo. I [moduli smart card offrono](/previous-versions/windows/desktop/secsmart/smart-card-modules) funzionalità simili.\]

Il metodo **Verify** costruisce un comando APDU [*(Application Protocol Data*](../secgloss/a-gly.md) Unit) che avvia il confronto (nella scheda) dei dati di verifica inviati dal dispositivo di interfaccia con i dati di riferimento archiviati nella scheda (ad esempio, la password).

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

*byRefCtrl* \[ Pollici\]
</dt> <dd>

Quantificatore dei dati di riferimento. Segue la codifica del controllo di riferimento P2.

Quando il corpo è vuoto, il comando può essere usato per recuperare il numero "X" di ulteriori tentativi consentiti (SW1-SW2=63CX) o per verificare se la verifica non è necessaria (SW1-SW2=9000).



| Valore                                                                                                                                                                                    | Significato                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="No_Info"></span><span id="no_info"></span><span id="NO_INFO"></span><dl> <dt>**Nessuna informazione**</dt> </dl>                     | Posizione bit: 00000000<br/> P2=00 è riservato per indicare che non viene usato alcun qualificatore specifico nelle schede in cui il comando verify fa riferimento ai dati segreti in modo non ambiguo.<br/> |
| <span id="Global_Ref"></span><span id="global_ref"></span><span id="GLOBAL_REF"></span><dl> <dt>**Riferimento globale**</dt> </dl>         | Posizione bit: 0-------<br/> Un esempio di riferimento globale è una password.<br/>                                                                                                        |
| <span id="Specific_Ref"></span><span id="specific_ref"></span><span id="SPECIFIC_REF"></span><dl> <dt>**Riferimento specifico**</dt> </dl> | Posizione bit: 1-------<br/> Un esempio di riferimento specifico è la password specifica di DF.<br/>                                                                                                  |
| <span id="RFU"></span><span id="rfu"></span><dl> <dt>**Rfu**</dt> </dl>                                                           | Posizione del bit: -xx-----<br/>                                                                                                                                                                 |
| <span id="Ref_Data__"></span><span id="ref_data__"></span><span id="REF_DATA__"></span><dl> <dt>**Dati di riferimento \#**</dt> </dl>        | Posizione dei bit: ---xxxxx<br/> Il numero di dati di riferimento può essere, ad esempio, un numero di password o un identificatore di EF breve.<br/>                                                           |



 

</dd> <dt>

*pData* \[ Pollici\]
</dt> <dd>

Puntatore ai dati di verifica. Questo parametro può essere **NULL**. Il valore predefinito è **NULL**.

</dd> <dt>

*ppCmd* \[ in, out\]
</dt> <dd>

Nell'input, un puntatore a un [**oggetto interfaccia ISCardCmd**](iscardcmd.md) o **NULL.**

Al ritorno, viene riempito con il comando APDU costruito da questa operazione. Se *ppCmd è* stato impostato su **NULL,** [**smart card'oggetto ISCardCmd**](iscardcmd.md) viene creato internamente e restituito usando il *puntatore ppCmd.* [](../secgloss/s-gly.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce uno dei valori possibili seguenti.



| Codice restituito                                                                                   | Descrizione                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operazione riuscita.<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | È stato usato un parametro non valido.<br/> |
| <dl> <dt>**PUNTATORE \_ E**</dt> </dl>     | È stato passato un puntatore non valido.<br/>            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insufficiente.<br/>                          |



 

## <a name="remarks"></a>Commenti

Lo stato di sicurezza può essere modificato in seguito a un confronto. I confronti non riusciti possono essere registrati nella scheda, ad esempio per limitare il numero di ulteriori tentativi di utilizzo dei dati di riferimento.

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

[**ISCardISO7816**](iscardiso7816.md)
</dt> </dl>

 

 
