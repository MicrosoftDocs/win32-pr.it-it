---
title: Struttura DLGITEMTEMPLATEEX
description: Blocco di testo utilizzato da un modello di finestra di dialogo esteso per descrivere la finestra di dialogo estesa. Per una descrizione del formato di un modello di finestra di dialogo esteso, vedere DLGTEMPLATEEX.
ms.assetid: c60fd8db-ee4b-433b-a2fb-68b9a677bac8
keywords:
- Finestre di dialogo della struttura DLGITEMTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGITEMTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ad2bf1795f5059ec1fdda00ddb6a93cfe396dae5b4119d392eff42382fa978b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118785867"
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

Identificatore del contesto della Guida per il controllo. Quando il sistema invia un [**messaggio WM \_ HELP,**](../shell/wm-help.md) passa il valore **helpID** nel membro **dwContextId** della [**struttura HELPINFO.**](/windows/win32/api/winuser/ns-winuser-helpinfo)

</dd> <dt>

**exStyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stili estesi per una finestra. Questo membro non viene usato per creare controlli nelle finestre di dialogo, ma le applicazioni che usano modelli di finestra di dialogo possono usarlo per creare altri tipi di finestre. Per un elenco di valori, vedere [**Stili finestra estesi**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stile del controllo. Questo membro può essere una combinazione di valori di stile della finestra [(](/windows/desktop/winmsg/window-styles) ad esempio **WS \_ BORDER**) e uno o più valori di stile del controllo [(](/windows/desktop/Controls/common-control-styles) ad esempio **BS \_ PUSHBUTTON** ed **ES \_ LEFT**).

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

**Cx**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Larghezza, in unità della finestra di dialogo, del controllo .

</dd> <dt>

**Cy**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Altezza, in unità della finestra di dialogo, del controllo .

</dd> <dt>

**id**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificatore del controllo.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **sz \_ \_ Ord**

</dd> <dd>

Matrice a lunghezza variabile di elementi a 16 bit che specifica la classe finestra del controllo. Se il primo elemento di questa matrice è un valore diverso da 0xFFFF, il sistema considera la matrice come una stringa Unicode con terminazione Null che specifica il nome di una classe finestra registrata.

Se il primo elemento è 0xFFFF, la matrice include un elemento aggiuntivo che specifica il valore ordinale di una classe di sistema predefinita. L'ordinale può essere uno dei valori atom seguenti.



| Valore                                                                             | Significato               |
|-----------------------------------------------------------------------------------|-----------------------|
| <dl> <dt>0x0080</dt> </dl> | Button<br/>     |
| <dl> <dt>0x0081</dt> </dl> | Modifica<br/>       |
| <dl> <dt>0x0082</dt> </dl> | Statica<br/>     |
| <dl> <dt>0x0083</dt> </dl> | Casella di riepilogo<br/>   |
| <dl> <dt>0x0084</dt> </dl> | Barra di scorrimento<br/> |
| <dl> <dt>0x0085</dt> </dl> | Casella combinata<br/>  |



 

</dd> <dt>

**title**
</dt> <dd>

Tipo: **sz \_ \_ Ord**

</dd> <dd>

Matrice a lunghezza variabile di elementi a 16 bit che contiene il testo iniziale o l'identificatore di risorsa del controllo. Se il primo elemento di questa matrice è 0xFFFF, la matrice include un elemento aggiuntivo che specifica il valore ordinale di una risorsa, ad esempio un'icona, in un file eseguibile. È possibile usare un identificatore di risorsa per i controlli, ad esempio i controlli icona statica, che caricano e visualizzano un'icona o un'altra risorsa anziché testo. Se il primo elemento è un valore diverso da 0xFFFF, il sistema considera la matrice come una stringa Unicode con terminazione Null che specifica il testo iniziale.

</dd> <dt>

**extraCount**
</dt> <dd>

Tipo: **WORD**

</dd> <dd>

Numero di byte di dati di creazione che seguono questo membro. Se questo valore è maggiore di zero, i dati di creazione iniziano in corrispondenza del limite **WORD** successivo. Questi dati di creazione possono essere di qualsiasi dimensione e formato. La routine della finestra del controllo deve essere in grado di interpretare i dati. Quando il sistema crea il controllo, passa un puntatore a questi dati nel *parametro lParam* del messaggio [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) inviato al controllo.

</dd> </dl>

## <a name="remarks"></a>Commenti

Un modello esteso per una finestra di dialogo è costituito da [**un'intestazione DLGTEMPLATEEX**](dlgtemplateex.md) seguita da una struttura **DLGITEMTEMPLATEEX** per ogni controllo nella finestra di dialogo.

Ogni **struttura DLGITEMTEMPLATEEX** deve essere allineata su un **limite DWORD.** Le matrici **windowClass** e **title** a lunghezza variabile devono essere allineate ai limiti **di WORD.** La matrice di dati di creazione, se presente, deve essere allineata su un limite **WORD.**

Se si specificano stringhe di caratteri **nelle matrici windowClass** e **title,** è necessario usare stringhe Unicode. Usare la [**funzione MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) per generare stringhe Unicode da stringhe ANSI.

I **membri x**, **y**, **cx** e **cy** specificano i valori nelle unità della finestra di dialogo. È possibile convertire questi valori in unità dello schermo (pixel) usando la [**funzione MapDialogRect.**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)

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

[**CREAZIONE \_ DI WM**](/windows/desktop/winmsg/wm-create)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**Multibytetowidechar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> <dt>

[**GUIDA DI \_ WM**](../shell/wm-help.md)
</dt> </dl>

 

