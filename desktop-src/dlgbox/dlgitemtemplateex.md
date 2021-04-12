---
title: Struttura DLGITEMTEMPLATEEX
description: Blocco di testo utilizzato da un modello di finestra di dialogo esteso per descrivere la finestra di dialogo estesa. Per una descrizione del formato di un modello di finestra di dialogo esteso, vedere DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Finestre di dialogo struttura DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7261fa832e5acfb4ef7d9723bc93b862947ef380
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400902"
---
# <a name="dlgitemtemplateex-structure"></a>Struttura DLGITEMTEMPLATEEX

Blocco di testo utilizzato da un modello di finestra di dialogo esteso per descrivere la finestra di dialogo estesa. Per una descrizione del formato di un modello di finestra di dialogo esteso, vedere [**DLGTEMPLATEEX**](dlgtemplateex.md).

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  short     x;
  short     y;
  short     cx;
  short     cy;
  DWORD     id;
  sz_Or_Ord windowClass;
  sz_Or_Ord title;
  WORD      extraCount;
} DLGITEMTEMPLATEEX;
```



## <a name="members"></a>Members

<dl> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificatore del contesto della Guida per il controllo. Quando il sistema invia un messaggio della [**\_ Guida WM**](../shell/wm-help.md) , passa il valore **HelpID** nel membro **dwContextId** della struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .

</dd> <dt>

**exStyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stili estesi per una finestra. Questo membro non viene utilizzato per creare controlli nelle finestre di dialogo, ma le applicazioni che utilizzano i modelli di finestra di dialogo possono utilizzarlo per creare altri tipi di finestre. Per un elenco di valori, vedere [**stili finestra estesa**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stile del controllo. Questo membro può essere una combinazione di [valori di stile della finestra](/windows/desktop/winmsg/window-styles) (ad esempio, il **\_ bordo WS**) e uno o più [valori dello stile del controllo](/windows/desktop/Controls/common-control-styles) , ad esempio il **\_ pulsante BS** e l' **es \_ Left**.

</dd> <dt>

**x**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Coordinata x, in unità della finestra di dialogo, dell'angolo superiore sinistro del controllo. Questa coordinata è sempre relativa all'angolo superiore sinistro dell'area client della finestra di dialogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Coordinata y, in unità della finestra di dialogo, dell'angolo superiore sinistro del controllo. Questa coordinata è sempre relativa all'angolo superiore sinistro dell'area client della finestra di dialogo.

</dd> <dt>

**CX**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Larghezza, in unità della finestra di dialogo, del controllo.

</dd> <dt>

**CY**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Altezza, in unità della finestra di dialogo, del controllo.

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificatore del controllo.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **SZ \_ o \_ ORD**

</dd> <dd>

Matrice a lunghezza variabile di elementi a 16 bit che specifica la classe della finestra del controllo. Se il primo elemento di questa matrice è un valore diverso da 0xFFFF, il sistema considera la matrice come una stringa Unicode con terminazione null che specifica il nome di una classe di finestre registrate.

Se il primo elemento è 0xFFFF, la matrice contiene un elemento aggiuntivo che specifica il valore ordinale di una classe di sistema predefinita. L'ordinale può essere uno dei valori Atom seguenti.



| Valore                                                                             | Significato               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>0x0080</dt> </dl> | Pulsante<br/>     |
| <dl> <dt>0x0081</dt> </dl> | Modifica<br/>       |
| <dl> <dt>0x0082</dt> </dl> | Static<br/>     |
| <dl> <dt>0x0083</dt> </dl> | Casella di riepilogo<br/>   |
| <dl> <dt>0x0084</dt> </dl> | Barra di scorrimento<br/> |
| <dl> <dt>0x0085</dt> </dl> | Casella combinata<br/>  |



 

</dd> <dt>

**title**
</dt> <dd>

Tipo: **SZ \_ o \_ ORD**

</dd> <dd>

Matrice a lunghezza variabile di elementi a 16 bit che contiene il testo iniziale o l'identificatore di risorsa del controllo. Se il primo elemento di questa matrice è 0xFFFF, la matrice contiene un elemento aggiuntivo che specifica il valore ordinale di una risorsa, ad esempio un'icona, in un file eseguibile. È possibile usare un identificatore di risorsa per i controlli, ad esempio i controlli icona statici, che caricano e visualizzano un'icona o un'altra risorsa anziché il testo. Se il primo elemento è un valore diverso da 0xFFFF, il sistema considera la matrice come una stringa Unicode con terminazione null che specifica il testo iniziale.

</dd> <dt>

**Numero di ripetizioni**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di byte di dati di creazione che seguono questo membro. Se questo valore è maggiore di zero, i dati di creazione iniziano al confine di **parola** successivo. I dati di creazione possono essere di qualsiasi dimensione e formato. La routine della finestra del controllo deve essere in grado di interpretare i dati. Quando il sistema crea il controllo, passa un puntatore a questi dati nel parametro *lParam* del messaggio [**WM \_ create**](/windows/desktop/winmsg/wm-create) inviato al controllo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un modello esteso per una finestra di dialogo è costituito da un'intestazione [**DLGTEMPLATEEX**](dlgtemplateex.md) seguita da una struttura **DLGITEMTEMPLATEEX** per ogni controllo nella finestra di dialogo.

Ogni struttura **DLGITEMTEMPLATEEX** deve essere allineata su un limite **DWORD** . Le matrici **WindowClass** e **title** a lunghezza variabile devono essere allineate sui limiti di **parola** . La matrice di dati di creazione, se presente, deve essere allineata su un confine di **parola** .

Se si specificano stringhe di caratteri nelle matrici **WindowClass** e **title** , è necessario utilizzare stringhe Unicode. Utilizzare la funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) per generare stringhe Unicode da stringhe ANSI.

I membri **x**, **y**, **CX** e **CY** specificano i valori nelle unità della finestra di dialogo. È possibile convertire questi valori in unità schermo (pixel) utilizzando la funzione [**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/> |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>       |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

**Riferimento**
</dt> <dt>

[**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)
</dt> <dt>

[**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama)
</dt> <dt>

[**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa)
</dt> <dt>

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGTEMPLATEEX**](dlgtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**creazione di WM \_**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**Guida di WM \_**](../shell/wm-help.md)
</dt> </dl>

 

