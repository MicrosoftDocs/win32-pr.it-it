---
title: EM_AUTOURLDETECT messaggio (Richedit.h)
description: Abilita o disabilita il rilevamento automatico dei collegamenti ipertestuali da parte di un controllo Rich Edit.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- EM_AUTOURLDETECT dei controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_AUTOURLDETECT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7c53df29b1d106c537543983f1734aef7facaaca5d0965c3a2588f285a7391
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049431"
---
# <a name="em_autourldetect-message"></a>Messaggio EM \_ AUTOURLDETECT

Abilita o disabilita il rilevamento automatico dei collegamenti ipertestuali da parte di un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specificare 0 per disabilitare il rilevamento automatico dei collegamenti oppure uno dei valori seguenti per abilitare vari tipi di rilevamento.



| Valore                                                                                                                                                                                       | Significato                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**AURL \_ DISABLEMIXEDLGC**</dt> </dl>          | **Windows 8**: disabilitare il riconoscimento dei nomi di dominio che contengono etichette con caratteri appartenenti a più di uno degli script seguenti: latino, greco e cirillico. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**AURL \_ ENABLEDRIVELETTERS**</dt> </dl> | **Windows 8**: riconoscere i nomi di file con una specifica di unità iniziale, ad esempio c: \\ temp.<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**AURL \_ ENABLEEA**</dt> </dl>                               | Questo valore è deprecato. in **alternativa, usare AURL \_ ENABLEEAURLS.**<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**AURL \_ ENABLEEAURLS**</dt> </dl>                   | Riconoscere gli URL che contengono caratteri dell'Asia orientale. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**AURL \_ ENABLEEMAILADDR**</dt> </dl>          | **Windows 8:** riconoscere gli indirizzi di posta elettronica.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**AURL \_ ENABLETELNO**</dt> </dl>                      | **Windows 8:** riconoscere i numeri di telefono.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**AURL \_ ENABLEURL**</dt> </dl>                            | **Windows 8**: riconoscere gli URL che includono il percorso.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro determina gli schemi URL riconosciuti se **AURL \_ ENABLEURL** è attivo. Se *lParam* è NULL, viene usato l'elenco dei nomi di schema predefinito (vedere la sezione Osservazioni). In alternativa, *lParam* può puntare a una stringa con terminazione Null costituita da un massimo di 50 nomi di schema con terminazione di due punti che sorrendono l'elenco dei nomi di schema predefinito. Ad esempio, la stringa potrebbe essere "news:http:ftp:telnet:". La sintassi del nome dello schema è definita nel documento [Uniform Resource Identifier (URI): Sintassi]( https://www.ietf.org/rfc/rfc2396.txt) generica nel sito Web IETF (Internet Engineering Task Force). In particolare, un nome di schema può contenere fino a 13 caratteri (inclusi i due punti), deve iniziare con un carattere alfabetico ASCII e può essere seguito da una combinazione di caratteri alfabetici ASCII, cifre e tre caratteri di punteggiatura: ".", "+" e "-". Il tipo di stringa può essere **char _ o \* *_* WCHAR. \*** Il controllo Rich Edit rileva automaticamente il tipo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è zero.

Se il messaggio ha esito negativo, il valore restituito è un valore diverso da zero. Ad esempio, il messaggio potrebbe non riuscire a causa di memoria insufficiente, un'opzione di rilevamento non valida o una stringa del nome di schema non valida.

Se *lParam* contiene più di 50 nomi di schema, il messaggio ha esito negativo con il valore restituito **E \_ INVALIDARG**.

## <a name="remarks"></a>Commenti

Se è abilitato il rilevamento automatico degli URL (ovvero *wParam* include **AURL \_ ENABLEURL),** il controllo Rich Edit analizza qualsiasi testo modificato per determinare se il testo corrisponde al formato di un URL (o più in generale in Windows 8 o versioni successive un IRI International Resource Identifier). Se *lParam* è NULL, il controllo rileva gli URL che iniziano con i nomi di schema seguenti:

-   callto
-   file
-   ftp
-   gopher
-   http
-   https
-   mailto
-   news
-   di HDInsight
-   Nntp
-   onenote
-   Outlook
-   taso
-   tel
-   telnet
-   wais
-   webcal

Quando il rilevamento automatico dei collegamenti è abilitato, il controllo Rich Edit rimuove l'effetto **CFE \_ LINK** dal testo modificato che non ha un formato riconosciuto dal controllo. Se l'applicazione usa **l'effetto CFE \_ LINK** per contrassegnare altri tipi di testo, non abilitare il rilevamento automatico dei collegamenti. Il controllo Rich Edit non controlla se esiste un collegamento rilevato. tale responsabilità appartiene al client.

Un controllo Rich Edit invia la [notifica EN \_ LINK](en-link.md) quando riceve vari messaggi mentre il puntatore del mouse è posizionato sul testo con l'effetto **CFE \_ LINK.** Per altre informazioni, vedere [Automatic RichEdit Hyperlinks (Collegamenti ipertestuali RichEdit automatici)](/archive/blogs/murrays/automatic-richedit-hyperlinks) e [RichEdit Friendly Name Hyperlinks (Collegamenti ipertestuali con nome descrittivo RichEdit).](/archive/blogs/murrays/richedit-friendly-name-hyperlinks)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[COLLEGAMENTO \_ EN](en-link.md)
</dt> </dl>

 

