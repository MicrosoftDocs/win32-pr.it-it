---
title: Messaggio di EM_SETCHARFORMAT (RichEdit. h)
description: Imposta la formattazione carattere in un controllo Rich Edit.
ms.assetid: 5e7a545d-4ca4-4dc6-badb-584c11194982
keywords:
- Controlli di Windows Message EM_SETCHARFORMAT
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
ms.openlocfilehash: ba8f37960659f29dd33d5b8f27f0b5a2e3d35eb0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104121042"
---
# <a name="em_setcharformat-message"></a>\_Messaggio SETCHARFORMAT em

Imposta la formattazione carattere in un controllo Rich Edit.

## <a name="parameters"></a>Parametri

<dl> <dt>

*wParam* 
</dt> <dd>

Formattazione dei caratteri applicata al controllo. Se questo parametro è zero, viene impostato il formato carattere predefinito. In caso contrario, può essere uno dei valori seguenti.



| Valore                                                                                                                                                                           | Significato                                                                                                                                                                                                                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SCF_ALL"></span><span id="scf_all"></span><dl> <dt>**\_tutti gli SCF**</dt> </dl>                                     | Applica la formattazione a tutto il testo nel controllo. Non valido con **l' \_ opzione SCF Selection** o **SCF \_ Word**.<br/>                                                                                                                                                                                         |
| <span id="SCF_ASSOCIATEFONT"></span><span id="scf_associatefont"></span><dl> <dt>**\_ASSOCIATEFONT SCF**</dt> </dl>       | **Richedit 4,1:** Associa un tipo di carattere a uno script specificato, modificando in questo modo il tipo di carattere predefinito per lo script. Per specificare il tipo di carattere, usare i membri seguenti di [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID**.<br/>                     |
| <span id="SCF_ASSOCIATEFONT2"></span><span id="scf_associatefont2"></span><dl> <dt>**\_ASSOCIATEFONT2 SCF**</dt> </dl>    | **Richedit 4,1:** Associa un tipo di carattere surrogato (piano 2) a uno script specificato, modificando in tal modo il tipo di carattere predefinito per lo script. Per specificare il tipo di carattere, usare i membri seguenti di [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a): **yHeight**, **bCharSet**, **bPitchAndFamily**, **szFaceName** e **LCID**.<br/> |
| <span id="SCF_CHARREPFROMLCID"></span><span id="scf_charrepfromlcid"></span><dl> <dt>**\_CHARREPFROMLCID SCF**</dt> </dl> | Ottiene il repertorio di caratteri dall'LCID.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_DEFAULT"></span><span id="scf_default"></span><dl> <dt>**\_impostazione predefinita SCF**</dt> </dl>                         | **Richedit 4,1:** Imposta il tipo di carattere predefinito per il controllo. <br/>                                                                                                                                                                                                                                      |
| <span id="SPF_DONTSETDEFAULT"></span><span id="spf_dontsetdefault"></span><dl> <dt>**\_DONTSETDEFAULT SPF**</dt> </dl>    | Impedisce l'impostazione del formato di paragrafo predefinito quando il controllo Rich Edit è vuoto.<br/>                                                                                                                                                                                                             |
| <span id="SCF_NOKBUPDATE"></span><span id="scf_nokbupdate"></span><dl> <dt>**\_NOKBUPDATE SCF**</dt> </dl>                | **Richedit 4,1:** Impedisce il cambio di tastiera per la corrispondenza con il tipo di carattere. Se, ad esempio, viene impostato un tipo di carattere arabo, in genere la funzione di tastiera automatica per i linguaggi BiDi modifica la tastiera in una tastiera araba.<br/>                                                                                 |
| <span id="SCF_SELECTION"></span><span id="scf_selection"></span><dl> <dt>**\_selezione SCF**</dt> </dl>                   | Applica la formattazione alla selezione corrente. Se la selezione è vuota, la formattazione dei caratteri viene applicata al punto di inserimento e il nuovo formato carattere è attivo solo fino a quando il punto di inserimento non viene modificato.<br/>                                                                      |
| <span id="SPF_SETDEFAULT"></span><span id="spf_setdefault"></span><dl> <dt>**\_impostazione predefinita SPF**</dt> </dl>                | Imposta gli attributi di formattazione dei paragrafi predefiniti.<br/>                                                                                                                                                                                                                                              |
| <span id="SCF_SMARTFONT"></span><span id="scf_smartfont"></span><dl> <dt>**\_SMARTFONT SCF**</dt> </dl>                   | Applicare il tipo di carattere solo se è in grado di gestire lo script.<br/>                                                                                                                                                                                                                                                   |
| <span id="SCF_USEUIRULES"></span><span id="scf_useuirules"></span><dl> <dt>**\_USEUIRULES SCF**</dt> </dl>                | **Richedit 4,1:** Utilizzato con **la \_ selezione SCF**. Indica che il formato proviene da una barra degli strumenti o da un altro strumento dell'interfaccia utente, quindi è necessario utilizzare le regole di formattazione dell'interfaccia utente anziché la formattazione letterale<br/>                                                                                                               |
| <span id="SCF_WORD"></span><span id="scf_word"></span><dl> <dt>**\_parola SCF**</dt> </dl>                                  | Applica la formattazione alla parola o alle parole selezionate. Se la selezione è vuota ma il punto di inserimento si trova all'interno di una parola, la formattazione viene applicata alla parola. Il valore della **\_ parola SCF** deve essere utilizzato insieme al valore **di \_ selezione SCF** .<br/>                                        |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Puntatore a una struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) che specifica la formattazione dei caratteri da usare. Vengono modificati solo gli attributi di formattazione specificati dal membro **dwMask** .

Microsoft Rich Edit 2,0 e versioni successive: questo parametro può essere un puntatore a una struttura [**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a) , che è un'estensione della struttura [**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata) . Prima di inviare il messaggio **\_ SETCHARFORMAT em** , impostare il membro **cbSize** della struttura su `sizeof(CHARFORMAT)` o `sizeof(CHARFORMAT2)` indicare quale versione della struttura viene utilizzata.

I membri **szFaceName** e **bCharSet** possono essere sovraregolati quando non sono validi per i caratteri, ad esempio: Arial in caratteri kanji.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Se l'operazione ha esito positivo, il valore restituito è un valore diverso da zero.

Se l'operazione ha esito negativo, il valore restituito è zero.

## <a name="remarks"></a>Commenti

Se questo messaggio viene inviato più di una volta con gli stessi parametri, l'effetto sul testo viene attivato o disattivato. Ovvero inviando il messaggio una volta generato l'effetto, l'invio del messaggio due volte Annulla l'effetto e così via.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2003\]<br/>                                  |
| Intestazione<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CHARFORMAT**](/windows/win32/api/richedit/ns-richedit-charformata)
</dt> <dt>

[**CHARFORMAT2**](/windows/desktop/api/Richedit/ns-richedit-charformat2a)
</dt> </dl>

 

 





