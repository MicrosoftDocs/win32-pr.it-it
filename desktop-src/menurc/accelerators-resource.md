---
title: Risorsa ACCELERATORS
description: Definisce uno o più acceleratori per un'applicazione. Un tasto di scelta rapida è una sequenza di tasti definita dall'applicazione per offrire all'utente un modo rapido per eseguire un'attività.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menu delle risorse ACCELERATORS e altre risorse
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e7ba2d19bbab6346f7a62afe56269f762cd94f7ef1730654fb6ac1abf317e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118235740"
---
# <a name="accelerators-resource"></a>Risorsa ACCELERATORS

Definisce uno o più acceleratori per un'applicazione. Un tasto di scelta rapida è una sequenza di tasti definita dall'applicazione per offrire all'utente un modo rapido per eseguire un'attività.

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

Nome univoco o valore intero senza segno a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*istruzioni facoltative*
</dt> <dd>

Zero o più delle istruzioni seguenti.



| Istruzione                                                        | Descrizione                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CHARACTERISTICS**](characteristics-statement.md) *dword*     | Informazioni definite dall'utente su una risorsa che possono essere usate dagli strumenti che leggono e scrivono file di risorse. Per altre informazioni, vedere [**CHARACTERISTICS.**](characteristics-statement.md) |
| [**LANGUAGE**](language-statement.md) *language*, *sottolinguaggio* | Specifica la lingua per la risorsa. Per altre informazioni, vedere [**LANGUAGE.**](language-statement.md)                                                                              |
| [**VERSION**](version-statement.md) *dword*                     | Numero di versione definito dall'utente per la risorsa che può essere usato dagli strumenti che leggono e scrivono file di risorse. Per altre informazioni, vedere [**VERSION.**](version-statement.md)              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*Evento*
</dt> <dd>

Sequenza di tasti da usare come tasto di scelta rapida. Può essere uno dei tipi di carattere seguenti.



| Tipo                    | Descrizione                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*char*"                | Singolo carattere racchiuso tra virgolette doppie ("). Il carattere può essere preceduto da un punto di controllo (^), vale a dire che è un carattere di controllo.                                                                                  |
| *Carattere*             | Valore intero che rappresenta un carattere. Il *parametro* di tipo deve essere **ASCII.**                                                                                                                                                           |
| *virtual-key character* | Valore intero che rappresenta una chiave virtuale. La chiave virtuale per le chiavi alfanumeriche può essere specificata inserendo la lettera o il numero maiuscolo tra virgolette doppie ,ad esempio "9" o "C". Il *parametro di* tipo deve essere **VIRTKEY.** |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idvalue*
</dt> <dd>

Valore intero senza segno a 16 bit che identifica l'acceleratore.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*digitare*
</dt> <dd>

Obbligatorio solo quando *il parametro* dell'evento *è un* carattere o un carattere di *chiave virtuale*. Il *parametro* di tipo specifica **ASCII** o **VIRTKEY**; Il valore intero *dell'evento* viene interpretato di conseguenza. Quando **si specifica VIRTKEY** e *l'evento* contiene una stringa, *l'evento* deve essere in maiuscolo.

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*Opzioni*
</dt> <dd>

Opzioni che definiscono l'acceleratore. Questo parametro può essere uno o più dei valori seguenti.



| Opzione                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **NOINVERT**                       | Specifica che non viene evidenziata alcuna voce di menu di primo livello quando viene usato il tasto di scelta rapida. Ciò è utile quando si definiscono i tasti di scelta rapida per azioni quali lo scorrimento che non corrispondono a una voce di menu. Se **NOINVERT viene** omesso, quando si usa l'acceleratore viene evidenziata una voce di menu di primo livello (se possibile). Questo attributo è obsoleto e viene mantenuto solo per garantire la compatibilità con le versioni precedenti dei file di risorse progettati per le versioni Windows. |
| **ALT**                            | Determina l'attivazione del tasto di scelta rapida solo se alt è premuto. Si applica solo alle chiavi virtuali.                                                                                                                                                                                                                                                                                                                                            |
| **Maiusc**                          | Determina l'attivazione del tasto di scelta rapida solo se MAIUSC è premuto. Si applica solo alle chiavi virtuali                                                                                                                                                                                                                                                                                                                                           |
| [**Controllo**](control-control.md) | Definisce il carattere come carattere di controllo (il tasto di scelta rapida viene attivato solo se il tasto CTRL è premuto). Questa operazione ha lo stesso effetto dell'uso di un punto di controllo (^) prima del carattere di acceleratore nel *parametro dell'evento.* Si applica solo alle chiavi virtuali                                                                                                                                                                                           |



 

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse.](common-resource-attributes.md)

## <a name="remarks"></a>Commenti

La [**funzione TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) viene usata per convertire i messaggi dei tasti di scelta rapida dalla coda dell'applicazione in [**messaggi WM \_ COMMAND**](./wm-command.md) [**o WM \_ SYSCOMMAND.**](./wm-syscommand.md)

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'uso dei tasti di scelta rapida.

``` syntax
1 ACCELERATORS
{
  "^C",  IDDCLEAR         ; control C
  "K",   IDDCLEAR         ; shift K
  "k",   IDDELLIPSE, ALT  ; alt k
  98,    IDDRECT, ASCII   ; b
  66,    IDDSTAR, ASCII   ; B (shift b)
  "g",   IDDRECT          ; g
  "G",   IDDSTAR          ; G (shift G)
  VK_F1, IDDCLEAR, VIRTKEY                ; F1
  VK_F1, IDDSTAR, CONTROL, VIRTKEY        ; control F1
  VK_F1, IDDELLIPSE, SHIFT, VIRTKEY       ; shift F1
  VK_F1, IDDRECT, ALT, VIRTKEY            ; alt F1
  VK_F2, IDDCLEAR, ALT, SHIFT, VIRTKEY    ; alt shift F2
  VK_F2, IDDSTAR, CONTROL, SHIFT, VIRTKEY ; ctrl shift F2
  VK_F2, IDDRECT, ALT, CONTROL, VIRTKEY   ; alt control F2
}
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso dei tasti di scelta rapida](./using-keyboard-accelerators.md)
</dt> <dt>

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**Caratteristiche**](characteristics-statement.md)
</dt> <dt>

[**Dialogo**](dialog-resource.md)
</dt> <dt>

[**Lingua**](language-statement.md)
</dt> <dt>

[**Menu**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**Stringtable**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 