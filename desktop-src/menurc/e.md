---
title: E (menu e altre risorse)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4f2423b002afe055c425978a643753e029d817eee5e7eccfc4379d2410f88ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461251"
---
# <a name="e-menus-and-other-resources"></a>E (menu e altre risorse)

[A](a.md) [B](b.md) [C](c.md) D E [F](f.md) G H [I](i.md) J K L M [N](n.md) [O](o.md) P Q R [S](r.md) T [U](t.md) [](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Menu vuoti non consentiti**
</dt> <dd>

Una **parola chiave END** viene visualizzata prima che le voci di menu siano definite nell'istruzione [**MENU.**](menu-resource.md) I menu vuoti non sono consentiti da Microsoft Windows 32 Resource Compiler (RC). Assicurarsi di non avere virgolette di apertura all'interno **dell'istruzione MENU.**

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**PREVISTO END nella finestra di dialogo**
</dt> <dd>

La **parola chiave END** deve essere visualizzata alla fine di un'istruzione [**DIALOG.**](dialog-resource.md) Assicurarsi che non siano presenti virgolette di apertura dall'istruzione precedente.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**PREVISTO END nel menu**
</dt> <dd>

La **parola chiave END** deve essere visualizzata alla fine di un'istruzione [**MENU.**](menu-resource.md) Assicurarsi che non siano presenti istruzioni **BEGIN** ed **END** non corrispondenti.

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Errore durante la creazione del nome della risorsa**
</dt> <dd>

Microsoft Windows 32 Resource Compiler (RC) non è in grado di creare la risorsa binaria specificata (. RES). Assicurarsi che non venga creato in un'unità di sola lettura. Usare **l'opzione /v** per determinare se il file viene creato.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Prevista virgola nella tabella dei tasti di scelta rapida**
</dt> <dd>

Microsoft Windows 32 Resource Compiler (RC) richiede una virgola tra i parametri *event* e *idvalue* nell'istruzione [**ACCELERATORS.**](accelerators-resource.md)

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Previsto nome della classe di controllo**
</dt> <dd>

Il *parametro* di classe di un'istruzione [**CONTROL**](control-control.md) nell'istruzione [**DIALOG**](dialog-resource.md) deve essere uno dei tipi di controllo **seguenti: BUTTON,** [**COMBOBOX,**](combobox-control.md) **EDIT,** [**LISTBOX,**](listbox-control.md) [**SCROLLBAR,**](scrollbar-control.md) **STATIC** o definito dall'utente. Assicurarsi che la classe sia digitata correttamente.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Previsto nome del viso del tipo di carattere**
</dt> <dd>

Il *parametro typeface* dell'istruzione **FONT** nell'istruzione [**DIALOG**](dialog-resource.md) deve essere una stringa di caratteri racchiusa tra virgolette doppie ("). Questo parametro specifica il nome di un tipo di carattere.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Valore ID previsto per Menuitem**
</dt> <dd>

[**L'istruzione MENU**](menu-resource.md) deve contenere [**un'istruzione MENUITEM,**](menuitem-statement.md) che include un numero intero o una costante simbolica nel *parametro MenuID.*

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Prevista stringa di menu**
</dt> <dd>

Ogni [**istruzione MENUITEM**](menuitem-statement.md) e [**POPUP**](popup-resource.md) deve contenere un *parametro di* testo. Questo parametro è una stringa racchiusa tra virgolette doppie (") che specifica il nome della voce di menu o del menu a comparsa. **Un'istruzione MENUITEM SEPARATOR** non richiede alcuna stringa tra virgolette.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Previsto valore numerico del comando**
</dt> <dd>

Microsoft Windows Resource Compiler (RC) prevedeva un parametro *idvalue* numerico [**nell'istruzione ACCELERATORS.**](accelerators-resource.md) Assicurarsi di aver usato un'istruzione [**\# define**](-define.md) per specificare il valore e che la costante usata sia stata digitata correttamente.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Prevista costante numerica nella tabella di stringhe**
</dt> <dd>

Una costante numerica, definita in un'istruzione [**\# define,**](-define.md) deve seguire immediatamente la parola chiave **BEGIN** in un'istruzione [**STRINGTABLE.**](stringtable-resource.md)

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Dimensioni in punti numeriche previste**
</dt> <dd>

Il *parametro pointsize* dell'istruzione [**FONT**](font-statement.md) nell'istruzione [**DIALOG**](dialog-resource.md) deve essere un valore integer di dimensioni in punti.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Prevista costante numerica dialog**
</dt> <dd>

[**Un'istruzione DIALOG**](dialog-resource.md) richiede valori interi per *i parametri x*, *y*, *width* *e height.* Assicurarsi che questi valori, inclusi dopo la parola chiave **DIALOG,** non siano negativi.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Prevista stringa in STRINGTABLE**
</dt> <dd>

È prevista una stringa dopo ogni parametro *stringid* numerico in [**un'istruzione STRINGTABLE.**](stringtable-resource.md)

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Previsto comando String o Constant Accelerator**
</dt> <dd>

Microsoft Windows Resource Compiler (RC) non è stato in grado di determinare quale chiave è stata impostata per l'acceleratore. Il *parametro dell'evento* nell'istruzione [**ACCELERATORS**](accelerators-resource.md) potrebbe non essere valido.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**Prevista parola chiave VALUE, BLOCK o END.**
</dt> <dd>

La [**struttura VERSIONINFO**](versioninfo-resource.md) richiede una **parola chiave VALUE,** **BLOCK** **o END.**

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Numero previsto per l'ID**
</dt> <dd>

È previsto un numero per il *parametro id* di un'istruzione [**CONTROL**](control-control.md) nell'istruzione [**DIALOG.**](dialog-resource.md) Assicurarsi di avere un numero o un'istruzione [**\# define**](-define.md) per l'identificatore di controllo.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Prevista stringa tra virgolette per la chiave**
</dt> <dd>

La stringa chiave che segue **la parola** chiave BLOCK o **VALUE** deve essere racchiusa tra virgolette doppie.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Prevista stringa tra virgolette nella classe dialog**
</dt> <dd>

Il *parametro class* dell'istruzione [**CLASS**](class-statement.md) nell'istruzione [**DIALOG**](dialog-resource.md) deve essere un numero intero o una stringa racchiusa tra virgolette doppie (").

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Prevista stringa tra virgolette nel titolo della finestra di dialogo**
</dt> <dd>

Il *parametro captiontext* dell'istruzione [**CAPTION**](caption-statement.md) nell'istruzione [**DIALOG**](dialog-resource.md) deve essere una stringa di caratteri racchiusa tra virgolette doppie (").

</dd> </dl>

 

 




