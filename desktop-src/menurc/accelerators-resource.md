---
title: Risorsa ACCELERAtori
description: Definisce uno o più acceleratori per un'applicazione. Un acceleratore è una sequenza di tasti definita dall'applicazione per fornire all'utente un modo rapido per eseguire un'attività.
ms.assetid: 5953ee2d-b7a7-45d2-8445-4cba1207e272
keywords:
- Menu risorse ACCELERAtori e altre risorse
topic_type:
- apiref
api_name:
- ACCELERATORS
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2aeb09ca52438f7b2f4903e5403eeb722e5d7d7
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104516750"
---
# <a name="accelerators-resource"></a>Risorsa ACCELERAtori

Definisce uno o più acceleratori per un'applicazione. Un acceleratore è una sequenza di tasti definita dall'applicazione per fornire all'utente un modo rapido per eseguire un'attività.

``` syntax
acctablename ACCELERATORS [optional-statements] {event, idvalue, [type] [options]... }
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="acctablename"></span><span id="ACCTABLENAME"></span>*acctablename*
</dt> <dd>

Nome univoco o valore Unsigned Integer a 16 bit che identifica la risorsa.

</dd> <dt>

<span id="optional-statements"></span><span id="OPTIONAL-STATEMENTS"></span>*facoltativo-istruzioni*
</dt> <dd>

Zero o più delle istruzioni seguenti.



| Istruzione                                                        | Descrizione                                                                                                                                                                             |
|------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Caratteristiche**](characteristics-statement.md) *DWORD*     | Informazioni definite dall'utente su una risorsa che possono essere usate da strumenti per la lettura e la scrittura di file di risorse. Per ulteriori informazioni, vedere [**caratteristiche**](characteristics-statement.md). |
| [](language-statement.md) *Lingua* lingua, *lingua* | Specifica la lingua per la risorsa. Per ulteriori informazioni, vedere [**Language**](language-statement.md).                                                                              |
| [](version-statement.md) *DWORD* versione                     | Numero di versione definito dall'utente per la risorsa che può essere usato da strumenti che leggono e scrivono file di risorse. Per ulteriori informazioni, vedere [**Version**](version-statement.md).              |



 

</dd> <dt>

<span id="event"></span><span id="EVENT"></span>*evento*
</dt> <dd>

Sequenza di tasti da utilizzare come tasto di scelta rapida. Può essere uno dei tipi di carattere seguenti.



| Tipo                    | Descrizione                                                                                                                                                                                                                                  |
|-------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "*char*"                | Carattere singolo racchiuso tra virgolette doppie ("). Il carattere può essere preceduto da un accento circonflesso (^), vale a dire che il carattere è un carattere di controllo.                                                                                  |
| *Carattere*             | Valore integer che rappresenta un carattere. Il parametro di *tipo* deve essere **ASCII**.                                                                                                                                                           |
| *carattere chiave virtuale* | Valore integer che rappresenta una chiave virtuale. È possibile specificare la chiave virtuale per le chiavi alfanumeriche inserendo la lettera o il numero maiuscolo tra virgolette doppie (ad esempio, "9" o "C"). Il parametro di *tipo* deve essere **VIRTKEY**. |



 

</dd> <dt>

<span id="idvalue"></span><span id="IDVALUE"></span>*idValue*
</dt> <dd>

valore Unsigned Integer a 16 bit che identifica il tasto di scelta rapida.

</dd> <dt>

<span id="type"></span><span id="TYPE"></span>*tipo*
</dt> <dd>

Obbligatorio solo quando il parametro dell' *evento* è un *carattere o un* carattere di *chiave virtuale*. Il parametro di *tipo* specifica **ASCII** o **VIRTKEY**; il valore integer dell' *evento* viene interpretato di conseguenza. Quando si specifica **VIRTKEY** e l' *evento* contiene una stringa, l' *evento* deve essere in maiuscolo.

</dd> <dt>

<span id="options"></span><span id="OPTIONS"></span>*Opzioni*
</dt> <dd>

opzioni che definiscono il tasto di scelta rapida. Il parametro può essere costituito da uno o più dei valori seguenti.



| Opzione                             | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Noinverte**                       | Specifica che non viene evidenziata alcuna voce di menu di primo livello quando si usa l'acceleratore. Questa operazione è utile quando si definiscono acceleratori per azioni quali lo scorrimento che non corrispondono a una voce di menu. Se si omette **NOinverted** , una voce di menu di primo livello verrà evidenziata (se possibile) quando si utilizza l'acceleratore. Questo attributo è obsoleto e viene mantenuto solo per compatibilità con le versioni precedenti dei file di risorse progettati per Windows a 16 bit. |
| **ALT**                            | Determina l'attivazione del tasto di scelta rapida solo se il tasto ALT è premuto. Si applica solo alle chiavi virtuali.                                                                                                                                                                                                                                                                                                                                            |
| **MAIUSC**                          | Determina l'attivazione dell'acceleratore solo se il tasto MAIUSC è premuto. Si applica solo alle chiavi virtuali                                                                                                                                                                                                                                                                                                                                           |
| [**CONTROLLO**](control-control.md) | Definisce il carattere come carattere di controllo. l'acceleratore viene attivato solo se la chiave del controllo è inattiva. Questa operazione ha lo stesso effetto dell'uso di un accento circonflesso (^) prima del carattere di accelerazione nel parametro dell' *evento* . Si applica solo alle chiavi virtuali                                                                                                                                                                                           |



 

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="remarks"></a>Commenti

La funzione [**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora) viene usata per convertire i messaggi acceleratore dalla coda dell'applicazione in messaggi [**WM \_ Command**](./wm-command.md) o [**WM \_ SYSCOMMAND**](./wm-syscommand.md) .

## <a name="examples"></a>Esempio

Nell'esempio seguente viene illustrato l'utilizzo dei tasti di scelta rapida.

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

[Uso di tasti di scelta rapida](./using-keyboard-accelerators.md)
</dt> <dt>

[**TranslateAccelerator**](/windows/win32/api/winuser/nf-winuser-translateacceleratora)
</dt> <dt>

[**CARATTERISTICHE**](characteristics-statement.md)
</dt> <dt>

[**DIALOGO**](dialog-resource.md)
</dt> <dt>

[**LINGUAGGIO**](language-statement.md)
</dt> <dt>

[**MENU**](menu-resource.md)
</dt> <dt>

[**RCDATA**](rcdata-resource.md)
</dt> <dt>

[**UN'STRINGTABLE**](stringtable-resource.md)
</dt> <dt>

[**Versione**](version-statement.md)
</dt> </dl>

 

 