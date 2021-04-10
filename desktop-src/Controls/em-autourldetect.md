---
title: Messaggio di EM_AUTOURLDETECT (RichEdit. h)
description: Abilita o Disabilita il rilevamento automatico dei collegamenti ipertestuali da un controllo Rich Edit.
ms.assetid: 6970ff36-ff3f-4413-a471-9389a76c8f38
keywords:
- Controlli di Windows Message EM_AUTOURLDETECT
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
ms.openlocfilehash: 5cc8f76b89e5e8aa529084b5c8c0898200e28ed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964482"
---
# <a name="em_autourldetect-message"></a>\_Messaggio AUTOURLDETECT em

Abilita o Disabilita il rilevamento automatico dei collegamenti ipertestuali da un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Specificare 0 per disabilitare il rilevamento automatico dei collegamenti oppure uno dei valori seguenti per abilitare vari tipi di rilevamento.



| Valore                                                                                                                                                                                       | Significato                                                                                                                                                                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="AURL_DISABLEMIXEDLGC"></span><span id="aurl_disablemixedlgc"></span><dl> <dt>**\_DISABLEMIXEDLGC AURL**</dt> </dl>          | **Windows 8**: disabilitare il riconoscimento dei nomi di dominio che contengono etichette con caratteri appartenenti a più di uno degli script seguenti: Latino, greco e cirillico. <br/> |
| <span id="AURL_ENABLEDRIVELETTERS"></span><span id="aurl_enabledriveletters"></span><dl> <dt>**\_ENABLEDRIVELETTERS AURL**</dt> </dl> | **Windows 8**: riconoscere i nomi di file con una specifica di unità, ad esempio c: \\ Temp.<br/>                                                                           |
| <span id="AURL_ENABLEEA"></span><span id="aurl_enableea"></span><dl> <dt>**\_ENABLEEA AURL**</dt> </dl>                               | Questo valore è deprecato; in alternativa, usare **AURL \_ ENABLEEAURLS** .<br/>                                                                                                            |
| <span id="AURL_ENABLEEAURLS"></span><span id="aurl_enableeaurls"></span><dl> <dt>**\_ENABLEEAURLS AURL**</dt> </dl>                   | Riconoscere gli URL che contengono caratteri asiatici orientali. <br/>                                                                                                                      |
| <span id="AURL_ENABLEEMAILADDR"></span><span id="aurl_enableemailaddr"></span><dl> <dt>**\_ENABLEEMAILADDR AURL**</dt> </dl>          | **Windows 8**: riconoscere gli indirizzi di posta elettronica.<br/>                                                                                                                                |
| <span id="AURL_ENABLETELNO"></span><span id="aurl_enabletelno"></span><dl> <dt>**\_ENABLETELNO AURL**</dt> </dl>                      | **Windows 8**: riconoscere i numeri di telefono.<br/>                                                                                                                              |
| <span id="AURL_ENABLEURL"></span><span id="aurl_enableurl"></span><dl> <dt>**\_ENABLEURL AURL**</dt> </dl>                            | **Windows 8**: riconoscere gli URL che includono il percorso.<br/>                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Questo parametro determina gli schemi URL riconosciuti se il **\_ ENABLEURL AURL** è attivo. Se *lParam* è null, viene usato l'elenco dei nomi di schema predefinito (vedere la sezione Osservazioni). In alternativa, *lParam* può puntare a una stringa con terminazione null costituita da un massimo di 50 nomi di schema con terminazione dei due punti che sostituiscono l'elenco dei nomi di schema predefiniti. Ad esempio, la stringa può essere "News: http: FTP: Telnet:". La sintassi del nome dello schema è definita nel sito Web dell' [URI (Uniform Resource Identifier): documento di sintassi generico]( https://www.ietf.org/rfc/rfc2396.txt) nel sito Web IETF (Internet Engineering Task Force). In particolare, un nome di schema può contenere un massimo di 13 caratteri (inclusi i due punti), deve iniziare con un carattere alfabetico ASCII e può essere seguito da una combinazione di alphabetics ASCII, cifre e tre caratteri di punteggiatura: ".", "+" e "-". Il tipo stringa può essere **char \** _ o _*WCHAR \**_. il controllo Rich Edit rileva automaticamente il tipo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se il messaggio ha esito positivo, il valore restituito è zero.

Se il messaggio ha esito negativo, il valore restituito è un valore diverso da zero. Ad esempio, il messaggio potrebbe non riuscire a causa di memoria insufficiente, un'opzione di rilevamento non valida o una stringa del nome di schema non valida.

Se _lParam * contiene più di 50 nomi di schema, il messaggio ha esito negativo con un valore restituito di **E \_ INVALIDARG**.

## <a name="remarks"></a>Commenti

Se il rilevamento automatico degli URL è abilitato, ovvero *wParam* include **AURL \_ ENABLEURL**, il controllo Rich Edit esegue l'analisi di qualsiasi testo modificato per determinare se il testo corrisponde al formato di un URL o, più in generale, in Windows 8 o versioni successive, un identificatore di risorsa internazionale IRI. Se *lParam* è null, il controllo rileva gli URL che iniziano con i nomi di schema seguenti:

-   callto
-   file
-   ftp
-   gopher
-   http
-   https
-   mailto
-   news
-   di HDInsight
-   NNTP
-   onenote
-   Outlook
-   Prospero
-   tel
-   telnet
-   wais
-   webcal

Quando il rilevamento automatico dei collegamenti è abilitato, il controllo Rich Edit rimuove l'effetto del **\_ collegamento CFE** dal testo modificato che non ha un formato riconosciuto dal controllo. Se l'applicazione usa l'effetto del **\_ collegamento CFE** per contrassegnare altri tipi di testo, non abilitare il rilevamento automatico dei collegamenti. Il controllo Rich Edit non controlla se esiste un collegamento rilevato; tale responsabilità appartiene al client.

Un controllo Rich Edit Invia la notifica di [ \_ collegamento en](en-link.md) quando riceve diversi messaggi quando il puntatore del mouse è sopra il testo con l'effetto del **\_ collegamento CFE** . Per ulteriori informazioni, vedere [collegamenti ipertestuali automatici RichEdit](/archive/blogs/murrays/automatic-richedit-hyperlinks) e [collegamenti ipertestuali con nome descrittivo](/archive/blogs/murrays/richedit-friendly-name-hyperlinks).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> <dt>

[\_collegamento en](en-link.md)
</dt> </dl>

 

