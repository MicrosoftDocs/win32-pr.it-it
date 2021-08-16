---
title: Parametri di controllo comuni
description: Di seguito viene descritta la sintassi generale per un'istruzione di definizione delle risorse di controllo.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abbdbf707e1ee72f62c7c08cb7065f4d1a4b8f2f4c000d52f3a28c9806a21a0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870562"
---
# <a name="common-control-parameters"></a>Parametri di controllo comuni

Di seguito viene descritta la sintassi generale per un'istruzione di definizione delle risorse di controllo. Il significato di ogni parametro è indicato di seguito. In alcuni casi, un'istruzione utilizzerà un parametro in modo diverso o potrebbe ignorare un parametro. La variazione specifica dell'istruzione è descritta nella documentazione relativa all'istruzione .

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Testo*
</dt> <dd>

Testo da visualizzare con il controllo . Il testo viene posizionato all'interno del controllo o adiacente al controllo.

Questo parametro deve contenere zero o più caratteri racchiusi tra virgolette doppie ("). Le stringhe vengono automaticamente con terminazione Null e convertite in Unicode nel file di risorse risultante.

Per impostazione predefinita, i caratteri elencati tra le virgolette doppie sono caratteri ANSI e le sequenze di escape vengono interpretate come sequenze di escape di byte. Se la stringa è preceduta dal prefisso "L", la stringa è una stringa di caratteri wide e le sequenze di escape vengono interpretate come sequenze di escape a 2 byte che specificano caratteri Unicode. Se nel testo è necessaria una virgoletta doppia, è necessario includere due volte le virgolette doppie.

Un carattere e commerciale (&) nel testo indica che il carattere seguente viene usato come carattere mnemoico per il controllo. Quando il controllo viene visualizzato, la e commerciale non viene visualizzata, ma il carattere mnemono è sottolineato. L'utente può scegliere il controllo premendo il tasto corrispondente al carattere mnemoico sottolineato. Per usare la e commerciale come carattere in una stringa, inserire due e commerciale (&&).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*Id*
</dt> <dd>

Identificatore del controllo. Questo valore deve essere un intero senza segno a 16 bit compreso nell'intervallo compreso tra 0 e 65.535 o una semplice espressione aritmetica che restituisce un valore in tale intervallo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*X*
</dt> <dd>

Coordinata X del lato sinistro del controllo rispetto al lato sinistro della finestra di dialogo. Questo valore deve essere un intero senza segno a 16 bit compreso tra 0 e 65.535. La coordinata è espressa in unità di dialogo ed è relativa all'origine della finestra di dialogo, della finestra o del controllo contenente il controllo specificato.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*Y*
</dt> <dd>

Coordinata Y del lato superiore del controllo rispetto alla parte superiore della finestra di dialogo. Questo valore deve essere un intero senza segno a 16 bit compreso tra 0 e 65.535. La coordinata è espressa in unità di dialogo relative all'origine della finestra di dialogo, della finestra o del controllo contenente il controllo specificato.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Larghezza*
</dt> <dd>

Larghezza del controllo. Questo valore deve essere un intero senza segno a 16 bit compreso tra 1 e 65.535. La larghezza è espressa in unità di 1/4 caratteri.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*Altezza*
</dt> <dd>

Altezza del controllo. Questo valore deve essere un intero senza segno a 16 bit compreso tra 1 e 65.535. L'altezza è in unità di 1/8 caratteri.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Stile*
</dt> <dd>

Stili dei controlli. Usare l'operatore OR bit per bit ( \| ) per combinare gli stili. Per altre informazioni, vedere [Stili delle finestre.](../winmsg/window-styles.md)

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*stile esteso*
</dt> <dd>

Stili di finestra estesi. È necessario specificare *style* per specificare *lo stile esteso.* Per altre informazioni, vedere [**EXSTYLE.**](exstyle-statement.md)

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*
</dt> <dd>

Espressione numerica che indica l'ID usato per identificare il controllo durante [**l'elaborazione \_ della Guida WM.**](../shell/wm-help.md)

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

Dati specifici del controllo per il controllo. Quando viene creata una finestra di dialogo e viene creato un controllo che contiene dati specifici del controllo, un puntatore a questi dati viene passato alla routine della finestra del controllo tramite *lParam* del messaggio [**WM \_ CREATE**](../winmsg/wm-create.md) per tale controllo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le unità di dialogo orizzontali sono 1/4 dell'unità di larghezza di base del dialogo. Le unità verticali sono 1/8 dell'unità di altezza di base del dialogo. Le unità di base del dialogo corrente vengono calcolate in base all'altezza e alla larghezza del tipo di carattere di sistema corrente. La [**funzione GetDialogBaseUnits restituisce**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) le unità di base del dialogo in pixel. Le coordinate sono relative all'origine della finestra di dialogo.

 

 