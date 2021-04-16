---
title: Struttura DLGTEMPLATEEX
description: Un modello di finestra di dialogo esteso inizia con un'intestazione DLGTEMPLATEEX che descrive la finestra di dialogo e specifica il numero di controlli nella finestra di dialogo.
ms.assetid: 9f016cc6-56e2-45d3-8773-1b405fc10d29
keywords:
- Finestre di dialogo struttura DLGTEMPLATEEX
topic_type:
- apiref
api_name:
- DLGTEMPLATEEX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1c3db7127e23e3133e11fe9c1600d37695e3b1ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518352"
---
# <a name="dlgtemplateex-structure"></a>Struttura DLGTEMPLATEEX

Un modello di finestra di dialogo esteso inizia con un'intestazione **DLGTEMPLATEEX** che descrive la finestra di dialogo e specifica il numero di controlli nella finestra di dialogo. Per ogni controllo in una finestra di dialogo, un modello di finestra di dialogo esteso ha un blocco di dati che usa il formato [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) per descrivere il controllo.

La struttura **DLGTEMPLATEEX** non è definita in alcun file di intestazione standard. La definizione della struttura è disponibile qui per spiegare il formato di un modello esteso per una finestra di dialogo.

## <a name="syntax"></a>Sintassi


```C++
typedef struct {
  WORD      dlgVer;
  WORD      signature;
  DWORD     helpID;
  DWORD     exStyle;
  DWORD     style;
  WORD      cDlgItems;
  short     x;
  short     y;
  short     cx;
  short     cy;
  sz_Or_Ord menu;
  sz_Or_Ord windowClass;
  WCHAR     title[titleLen];
  WORD      pointsize;
  WORD      weight;
  BYTE      italic;
  BYTE      charset;
  WCHAR     typeface[stringLen];
} DLGTEMPLATEEX;
```



## <a name="members"></a>Members

<dl> <dt>

**dlgVer**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di versione del modello della finestra di dialogo estesa. Questo membro deve essere impostato su 1.

</dd> <dt>

**URL REST**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Indica se un modello è un modello di finestra di dialogo esteso. Se **Signature** è 0xFFFF, si tratta di un modello di finestra di dialogo esteso. In questo caso, il membro **dlgVer** specifica il numero di versione del modello. Se **Signature** è un valore diverso da 0xFFFF, si tratta di un modello di finestra di dialogo standard che usa le strutture [**DLGTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgtemplate) e [**DLGITEMTEMPLATE**](/windows/desktop/api/Winuser/ns-winuser-dlgitemtemplate) .

</dd> <dt>

**helpID**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Identificatore del contesto della Guida per la finestra di dialogo. Quando il sistema invia un messaggio della [**\_ Guida WM**](../shell/wm-help.md) , questo valore viene passato nel membro **wContextId** della struttura [**HELPINFO**](/windows/win32/api/winuser/ns-winuser-helpinfo) .

</dd> <dt>

**exStyle**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stili estesi di Windows. Questo membro non viene utilizzato durante la creazione di finestre di dialogo, ma le applicazioni che utilizzano i modelli di finestra di dialogo possono utilizzarlo per creare altri tipi di finestre. Per un elenco di valori, vedere [**stili finestra estesa**](/windows/desktop/winmsg/extended-window-styles).

</dd> <dt>

**style**
</dt> <dd>

Tipo: **DWORD**

</dd> <dd>

Stile della finestra di dialogo. Questo membro può essere una combinazione di valori di [stile della finestra](/windows/desktop/winmsg/window-styles) e di valori di stile della finestra di [dialogo](dialog-box-styles.md).

Se **lo stile** include lo stile della finestra di dialogo DS **\_ sefont** o **DS \_ SHELLFONT** , l'intestazione **DLGTEMPLATEEX** del modello della finestra di dialogo estesa contiene quattro membri aggiuntivi ( **pointsize**, **Weight**, **Italic** e **Typeface**) che descrivono il tipo di carattere da utilizzare per il testo nell'area client e i controlli della finestra di dialogo. Se possibile, il sistema crea un tipo di carattere in base ai valori specificati in questi membri. Quindi, il sistema invia un messaggio di [**\_ tipo carattere di tipo WM**](/windows/desktop/winmsg/wm-setfont) alla finestra di dialogo e a ogni controllo per fornire un handle al tipo di carattere.

Per ulteriori informazioni, vedere [tipi di carattere della finestra di dialogo](about-dialog-boxes.md).

</dd> <dt>

**cDlgItems**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Numero di controlli nella finestra di dialogo.

</dd> <dt>

**x**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Coordinata x, in unità della finestra di dialogo, dell'angolo superiore sinistro della finestra di dialogo.

</dd> <dt>

**y**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Coordinata y, in unità della finestra di dialogo, dell'angolo superiore sinistro della finestra di dialogo.

</dd> <dt>

**CX**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Larghezza, in unità della finestra di dialogo, della finestra di dialogo.

</dd> <dt>

**CY**
</dt> <dd>

Tipo: **short**

</dd> <dd>

Altezza, in unità della finestra di dialogo, della finestra di dialogo.

</dd> <dt>

**menu**
</dt> <dd>

Tipo: **SZ \_ o \_ ORD**

</dd> <dd>

Matrice a lunghezza variabile di elementi a 16 bit che identifica una risorsa di menu per la finestra di dialogo. Se il primo elemento di questa matrice è 0x0000, alla finestra di dialogo non è associato alcun menu e la matrice non contiene altri elementi. Se il primo elemento è 0xFFFF, la matrice contiene un elemento aggiuntivo che specifica il valore ordinale di una risorsa di menu in un file eseguibile. Se il primo elemento ha un altro valore, il sistema considera la matrice come una stringa Unicode con terminazione null che specifica il nome di una risorsa di menu in un file eseguibile.

</dd> <dt>

**windowClass**
</dt> <dd>

Tipo: **SZ \_ o \_ ORD**

</dd> <dd>

Matrice a lunghezza variabile di elementi a 16 bit che identifica la classe della finestra della finestra di dialogo. Se il primo elemento della matrice è 0x0000, il sistema utilizza la classe della finestra di dialogo predefinita per la finestra di dialogo e la matrice non contiene altri elementi. Se il primo elemento è 0xFFFF, la matrice contiene un elemento aggiuntivo che specifica il valore ordinale di una classe di finestra di sistema predefinita. Se il primo elemento ha un altro valore, il sistema considera la matrice come una stringa Unicode con terminazione null che specifica il nome di una classe di finestre registrate.

</dd> <dt>

**title**
</dt> <dd>

Tipo: **WCHAR \[ titleLen \]**

</dd> <dd>

Titolo della finestra di dialogo. Se il primo elemento di questa matrice è 0x0000, la finestra di dialogo non ha alcun titolo e la matrice non contiene altri elementi.

</dd> <dt>

**pointsize**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Dimensioni in punti del tipo di carattere da utilizzare per il testo nella finestra di dialogo e i relativi controlli.

Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.

</dd> <dt>

**weight**
</dt> <dd>

Tipo: **Word**

</dd> <dd>

Spessore del tipo di carattere. Si noti che, anche se può essere uno qualsiasi dei valori elencati per il membro **lfWeight** della struttura [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta) , qualsiasi valore usato verrà automaticamente modificato in **FW \_ Normal**.

Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.

</dd> <dt>

**corsivo**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Indica se il tipo di carattere è in corsivo. Se questo valore è **true**, il tipo di carattere è in corsivo.

Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.

</dd> <dt>

**charset**
</dt> <dd>

Tipo: **byte**

</dd> <dd>

Set di caratteri da utilizzare. Per ulteriori informazioni, vedere il membro **lfCharSet** di [**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta).

Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.

</dd> <dt>

**carattere tipografico**
</dt> <dd>

Tipo: **WCHAR \[ stringLen \]**

</dd> <dd>

Nome del carattere tipografico per il tipo di carattere.

Questo membro è presente solo se il membro dello **stile** specifica **DS \_ sefont** o **DS \_ SHELLFONT**.

</dd> </dl>

## <a name="remarks"></a>Commenti

È possibile utilizzare un modello di finestra di dialogo esteso anziché un modello di finestra di dialogo standard nelle funzioni [**CreateDialogIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirectparama), [**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama), [**CreateDialogIndirect**](/windows/desktop/api/Winuser/nf-winuser-createdialogindirecta)e [**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta) .

La seguente intestazione **DLGTEMPLATEEX** in un modello di finestra di dialogo esteso è costituita da una o più strutture [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) che descrivono i controlli della finestra di dialogo. Il membro **cDlgItems** della struttura **DLGITEMTEMPLATEEX** specifica il numero di strutture **DLGITEMTEMPLATEEX** che seguono nel modello.

Ogni struttura [**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md) del modello deve essere allineata in un limite **DWORD** . Se il membro dello **stile** specifica lo stile DS **\_ sefont** o **DS \_ SHELLFONT** , la prima struttura **DLGITEMTEMPLATEEX** inizia sul primo limite **DWORD** dopo la stringa del **carattere tipografico** . Se questi stili non vengono specificati, la prima struttura inizia sul primo limite **DWORD** dopo la stringa del **titolo** .

Le matrici **menu**, **WindowClass**, **title** e **Typeface** devono essere allineate sui limiti di **parola** .

Se si specificano stringhe di caratteri nelle matrici **menu**, **WindowClass**, **title** e **Typeface** , è necessario utilizzare stringhe Unicode. Utilizzare la funzione [**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar) per generare queste stringhe Unicode dalle stringhe ANSI.

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

[**DialogBoxIndirect**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirecta)
</dt> <dt>

[**DialogBoxIndirectParam**](/windows/desktop/api/Winuser/nf-winuser-dialogboxindirectparama)
</dt> <dt>

[**DLGITEMTEMPLATEEX**](dlgitemtemplateex.md)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/Winuser/nf-winuser-mapdialogrect)
</dt> <dt>

[**\_tipo di carattere WM**](/windows/desktop/winmsg/wm-setfont)
</dt> <dt>

**Informazioni concettuali**
</dt> <dt>

[Finestre di dialogo](dialog-boxes.md)
</dt> <dt>

**Altre risorse**
</dt> <dt>

[**LOGFONT**](/windows/win32/api/wingdi/ns-wingdi-logfonta)
</dt> <dt>

[**MultiByteToWideChar**](/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar)
</dt> </dl>

 

