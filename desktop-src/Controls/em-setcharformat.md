---
title: EM_SETCHARFORMAT messaggio (Richedit.h)
description: Imposta la formattazione dei caratteri in un controllo Rich Edit.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- EM_SETCHARFORMAT controlli Windows messaggio
topic_type:
- apiref
api_name:
- EM_SETCHARFORMAT
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 100cfb1d322cde2d411a0298ee86c224899669defc585826b16bf96751bb4639
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118673131"
---
# <a name="em_setcharformat-message"></a>Messaggio \_ EM SETCHARFORMAT

Imposta la formattazione dei caratteri in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Formattazione dei caratteri applicata al controllo. Se questo parametro è zero, viene impostato il formato carattere predefinito. In caso contrario, può essere uno dei valori seguenti.



| Valore                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**SCF \_ ALL**</dt> </dl>                                     | Applica la formattazione a tutto il testo nel controllo . Non valido con **SCF \_ SELECTION** o **SCF \_ WORD.**<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**SCF \_ ASSOCIATEFONT**</dt> </dl>       | **RichEdit 4.1:** Associa un tipo di carattere a uno script specificato, modificando così il tipo di carattere predefinito per tale script. Per specificare il tipo di carattere, usare i membri seguenti di [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **lcid**.<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**SCF \_ ASSOCIATEFONT2**</dt> </dl>    | **RichEdit 4.1:** Associa un tipo di carattere surrogato (plane-2) a uno script specificato, modificando così il tipo di carattere predefinito per tale script. Per specificare il tipo di carattere, usare i membri seguenti di [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **lcid**.<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**SCF \_ CHARREPFROMLCID**</dt> </dl> | Ottiene l'elenco di caratteri dall'LCID.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**SCF \_ DEFAULT**</dt> </dl>                         | **RichEdit 4.1:** Imposta il tipo di carattere predefinito per il controllo. <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**SPF \_ DONTSETDEFAULT**</dt> </dl>    | Impedisce l'impostazione del formato di paragrafo predefinito quando il controllo Rich Edit è vuoto.<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**SCF \_ NOKBUPDATE**</dt> </dl>                | **RichEdit 4.1:** Impedisce il passaggio da tastiera in modo che corrisponda al tipo di carattere. Ad esempio, se è impostato un tipo di carattere arabo, in genere la funzionalità della tastiera automatica per le lingue Bidi cambia la tastiera in una tastiera araba.<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**SELEZIONE \_ SCF**</dt> </dl>                   | Applica la formattazione alla selezione corrente. Se la selezione è vuota, la formattazione dei caratteri viene applicata al punto di inserimento e il nuovo formato di carattere è attivo solo fino a quando il punto di inserimento non cambia.<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**SPF \_ SETDEFAULT**</dt> </dl>                | Imposta gli attributi di formattazione dei paragrafi predefiniti.<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**SCF \_ SMARTFONT**</dt> </dl>                   | Applicare il tipo di carattere solo se è in grado di gestire lo script.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**SCF \_ USEUIRULES**</dt> </dl>                | **RichEdit 4.1:** Usato con **SCF \_ SELECTION.** Indica che il formato deriva da una barra degli strumenti o da un altro strumento dell'interfaccia utente, pertanto è consigliabile usare le regole di formattazione dell'interfaccia utente anziché la formattazione letterale.<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**SCF \_ WORD**</dt> </dl>                                  | Applica la formattazione alla parola o alle parole selezionate. Se la selezione è vuota ma il punto di inserimento si trova all'interno di una parola, la formattazione viene applicata alla parola. Il **valore SCF \_ WORD** deve essere usato insieme al **valore SCF \_ SELECTION.**<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a [**una struttura CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) che specifica la formattazione dei caratteri da usare. Vengono modificati solo gli attributi di formattazione specificati dal membro **dwMask.**

Microsoft Rich Edit 2.0 e versioni successive: questo parametro può essere un puntatore a una [**struttura CHARFORMAT2,**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) che è un'estensione della [**struttura CHARFORMAT.**](/windows/win32/api/richedit/ns-richedit-charformata) Prima di inviare il messaggio **EM \_ SETCHARFORMAT,** impostare il membro **cbSize** della struttura su o indicare la versione `sizeof(CHARFORMAT)` della struttura in `sizeof(CHARFORMAT2)` uso.

I **membri szFaceName** e **bCharSet** possono essere ignorati quando non sono validi per i caratteri, ad esempio Arial sui caratteri kanji.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione non riesce, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Se questo messaggio viene inviato più volte con gli stessi parametri, l'effetto sul testo viene attivato o disattivato. In altre informazioni, l'invio del messaggio una volta produce l'effetto, l'invio del messaggio due volte annulla l'effetto e così via.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>Richedit.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





