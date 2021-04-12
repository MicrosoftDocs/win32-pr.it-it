---
title: Parametri di controllo comuni
description: Di seguito viene descritta la sintassi generale per un'istruzione di definizione delle risorse del controllo.
ms.assetid: e7a49a9f-93b5-4221-8006-3d1864b7a6a1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 261c71163276ed39841d6f6d7e125d4eb5420072
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337182"
---
# <a name="common-control-parameters"></a>Parametri di controllo comuni

Di seguito viene descritta la sintassi generale per un'istruzione di definizione delle risorse del controllo. Il significato di ogni parametro è riportato di seguito. Occasionalmente, un'istruzione utilizzerà un parametro in modo diverso o potrebbe ignorare un parametro. La variazione specifica dell'istruzione è descritta nella documentazione relativa all'istruzione.

``` syntax
control [[text,]] id, x, y, width, height[[, style[[, extended-style]]]][, helpId]
[{ data-element-1 [, data-element-2 [,  . . . ]]}]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*testo*
</dt> <dd>

Testo da visualizzare con il controllo. Il testo è posizionato all'interno del controllo o accanto al controllo.

Questo parametro deve contenere zero o più caratteri racchiusi tra virgolette doppie ("). Le stringhe vengono terminate automaticamente con terminazione null e convertite in Unicode nel file di risorse risultante.

Per impostazione predefinita, i caratteri elencati tra virgolette doppie sono caratteri ANSI e le sequenze di escape vengono interpretate come sequenze di escape di byte. Se la stringa è preceduta dal prefisso "L", la stringa è una stringa di caratteri wide e le sequenze di escape vengono interpretate come sequenze di escape da 2 byte che specificano caratteri Unicode. Se nel testo è richiesta una virgoletta doppia, è necessario includere due volte il segno di virgolette doppie.

Un carattere e commerciale (&) nel testo indica che il carattere seguente viene usato come carattere mnemonico per il controllo. Quando il controllo viene visualizzato, la e commerciale non viene visualizzata, ma il carattere mnemonico è sottolineato. L'utente può scegliere il controllo premendo il tasto corrispondente al carattere mnemonico sottolineato. Per utilizzare la e commerciale come carattere in una stringa, inserire due e commerciale (&&).

</dd> <dt>

<span id="id"></span><span id="ID"></span>*ID*
</dt> <dd>

Identificatore del controllo. Questo valore deve essere un Unsigned Integer a 16 bit nell'intervallo compreso tra 0 e 65.535 oppure una semplice espressione aritmetica che restituisce un valore in tale intervallo.

</dd> <dt>

<span id="x"></span><span id="X"></span>*x*
</dt> <dd>

Coordinata X del lato sinistro del controllo rispetto al lato sinistro della finestra di dialogo. Questo valore deve essere un Unsigned Integer a 16 bit nell'intervallo compreso tra 0 e 65.535. La coordinata si trova in unità di dialogo ed è relativa all'origine della finestra di dialogo, della finestra o del controllo contenente il controllo specificato.

</dd> <dt>

<span id="y"></span><span id="Y"></span>*y*
</dt> <dd>

Coordinata Y del lato superiore del controllo rispetto alla parte superiore della finestra di dialogo. Questo valore deve essere un Unsigned Integer a 16 bit nell'intervallo compreso tra 0 e 65.535. La coordinata è espressa in unità di dialogo relative all'origine della finestra di dialogo, della finestra o del controllo contenente il controllo specificato.

</dd> <dt>

<span id="width"></span><span id="WIDTH"></span>*Larghezza*
</dt> <dd>

Larghezza del controllo. Questo valore deve essere un Unsigned Integer a 16 bit compreso nell'intervallo da 1 a 65.535. La larghezza è in unità da 1 a 4 caratteri.

</dd> <dt>

<span id="height"></span><span id="HEIGHT"></span>*altezza*
</dt> <dd>

Altezza del controllo. Questo valore deve essere un Unsigned Integer a 16 bit compreso nell'intervallo da 1 a 65.535. L'altezza è in unità di 1/8 caratteri.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*stile*
</dt> <dd>

Stili del controllo. Utilizzare l'operatore OR bit \| per bit () per combinare gli stili. Per altre informazioni, vedere [stili di finestra](../winmsg/window-styles.md).

</dd> <dt>

<span id="extended-style"></span><span id="EXTENDED-STYLE"></span>*stile esteso*
</dt> <dd>

Stili estesi della finestra. È necessario specificare *lo stile* per specificare il *tipo esteso*. Per ulteriori informazioni, vedere [**ExStyle**](exstyle-statement.md).

</dd> <dt>

<span id="helpId"></span><span id="helpid"></span><span id="HELPID"></span>*helpId*
</dt> <dd>

Espressione numerica che indica l'ID utilizzato per identificare il controllo durante l'elaborazione della [**\_ Guida WM**](../shell/wm-help.md) .

</dd> <dt>

<span id="controlData"></span><span id="controldata"></span><span id="CONTROLDATA"></span>*controlData*
</dt> <dd>

Dati specifici del controllo per il controllo. Quando viene creata una finestra di dialogo e viene creato un controllo in tale finestra di dialogo con dati specifici del controllo, viene passato un puntatore a tali dati nella routine della finestra del controllo tramite il valore *lParam* del messaggio [**WM \_ create**](../winmsg/wm-create.md) per il controllo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Le unità di dialogo orizzontali sono 1/4 dell'unità della larghezza di base della finestra di dialogo. Le unità verticali sono 1/8 dell'unità di altezza di base della finestra di dialogo. Le unità di base della finestra di dialogo correnti vengono calcolate in base all'altezza e alla larghezza del tipo di carattere del sistema corrente. La funzione [**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits) restituisce le unità di base della finestra di dialogo in pixel. Le coordinate sono relative all'origine della finestra di dialogo.

 

 