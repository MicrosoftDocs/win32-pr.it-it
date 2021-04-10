---
title: E (menu e altre risorse)
description: A B C D E F G H I J K L M N O P Q R S T U V W X Y Z
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 14e12ba3-8451-4a93-a555-e1c9e6040a67
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029f8d26d341a114ab7bfeae269a391f8df90423
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "104118855"
---
# <a name="e-menus-and-other-resources"></a>E (menu e altre risorse)

[A](a.md) [B](b.md) [C](c.md) d E [F](f.md) G H [i](i.md) J K L M [N](n.md) [O](o.md) P Q [R](r.md) S [T](t.md) [U](u.md) [V](v.md) [W](w.md) X Y Z

<dl> <dt>

<span id="tools.e_1_gly"></span><span id="TOOLS.E_1_GLY"></span>**Menu vuoti non consentiti**
</dt> <dd>

Una parola chiave **end** viene visualizzata prima che tutte le voci di menu siano definite nell'istruzione di [**menu**](menu-resource.md) . I menu vuoti non sono consentiti dal compilatore di risorse Microsoft Windows 32 (RC). Assicurarsi che non siano presenti virgolette di apertura nell'istruzione di **menu** .

</dd> <dt>

<span id="tools.e_2_gly"></span><span id="TOOLS.E_2_GLY"></span>**FINE prevista nella finestra di dialogo**
</dt> <dd>

La parola chiave **end** deve essere visualizzata alla fine di un'istruzione della [**finestra di dialogo**](dialog-resource.md) . Verificare che non siano presenti virgolette di apertura rimaste nell'istruzione precedente.

</dd> <dt>

<span id="tools.e_3_gly"></span><span id="TOOLS.E_3_GLY"></span>**FINE prevista nel menu**
</dt> <dd>

La parola chiave **end** deve essere visualizzata alla fine di un'istruzione di [**menu**](menu-resource.md) . Verificare che non siano presenti istruzioni **Begin** e **end** non corrispondenti.

</dd> <dt>

<span id="tools.e_4_gly"></span><span id="TOOLS.E_4_GLY"></span>**Errore Creatingresource-nome**
</dt> <dd>

Il compilatore di risorse Microsoft Windows 32 (RC) non è riuscito a creare la risorsa binaria specificata (. File RES). Assicurarsi che non venga creato in un'unità di sola lettura. Usare l'opzione **/v** per verificare se il file è in fase di creazione.

</dd> <dt>

<span id="tools.e_5_gly"></span><span id="TOOLS.E_5_GLY"></span>**Prevista virgola nella tabella dei tasti di scelta rapida**
</dt> <dd>

Il compilatore di risorse Microsoft Windows 32 (RC) richiede una virgola tra i parametri *Event* e *idValue* nell'istruzione [**Accelerators**](accelerators-resource.md) .

</dd> <dt>

<span id="tools.e_6_gly"></span><span id="TOOLS.E_6_GLY"></span>**Previsto nome classe di controllo**
</dt> <dd>

Il parametro *Class* di un'istruzione di [**controllo**](control-control.md) nell'istruzione [**Dialog**](dialog-resource.md) deve essere uno dei seguenti tipi di controllo: **Button**, [**ComboBox**](combobox-control.md), **Edit**, [**ListBox**](listbox-control.md), [**ScrollBar**](scrollbar-control.md), **static** o definito dall'utente. Verificare che la classe sia stata digitata correttamente.

</dd> <dt>

<span id="tools.e_7_gly"></span><span id="TOOLS.E_7_GLY"></span>**Nome del tipo di carattere previsto**
</dt> <dd>

Il parametro *Typeface* dell'istruzione **font** nell'istruzione [**Dialog**](dialog-resource.md) deve essere una stringa di caratteri racchiusa tra virgolette doppie ("). Questo parametro specifica il nome di un tipo di carattere.

</dd> <dt>

<span id="tools.e_8_gly"></span><span id="TOOLS.E_8_GLY"></span>**Previsto valore ID per MenuItem**
</dt> <dd>

L'istruzione [**menu**](menu-resource.md) deve contenere un'istruzione [**MenuItem**](menuitem-statement.md) , che include un Integer o una costante simbolica nel parametro *menuID* .

</dd> <dt>

<span id="tools.e_9_gly"></span><span id="TOOLS.E_9_GLY"></span>**Prevista stringa di menu**
</dt> <dd>

Ogni istruzione [**MenuItem**](menuitem-statement.md) e [**popup**](popup-resource.md) deve contenere un parametro di *testo* . Questo parametro è una stringa racchiusa tra virgolette doppie (") che specifica il nome della voce di menu o del menu a comparsa. Un'istruzione del **separatore MenuItem** non richiede una stringa racchiusa tra virgolette.

</dd> <dt>

<span id="tools.e_10_gly"></span><span id="TOOLS.E_10_GLY"></span>**Previsto valore del comando numerico**
</dt> <dd>

Per il compilatore di risorse di Microsoft Windows (RC) era previsto un parametro numerico *idValue* nell'istruzione [**Accelerators**](accelerators-resource.md) . Assicurarsi di aver usato un'istruzione [**\# define**](-define.md) per specificare il valore e che la costante utilizzata sia stata digitata correttamente.

</dd> <dt>

<span id="tools.e_11_gly"></span><span id="TOOLS.E_11_GLY"></span>**Prevista costante numerica nella tabella di stringhe**
</dt> <dd>

Una costante numerica, definita in un'istruzione [**\# define**](-define.md) , deve seguire immediatamente la parola chiave **Begin** in un'istruzione [**un'STRINGTABLE**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_12_gly"></span><span id="TOOLS.E_12_GLY"></span>**Dimensioni previste per i punti numerici**
</dt> <dd>

Il parametro *pointsize* dell'istruzione [**font**](font-statement.md) nell'istruzione [**Dialog**](dialog-resource.md) deve essere un valore di dimensione in punti Integer.

</dd> <dt>

<span id="tools.e_13_gly"></span><span id="TOOLS.E_13_GLY"></span>**Prevista costante finestra di dialogo numerica**
</dt> <dd>

Un'istruzione della [**finestra di dialogo**](dialog-resource.md) richiede valori integer per i parametri *x*, *y*, *Width* e *Height* . Verificare che questi valori, inclusi dopo la parola chiave della **finestra di dialogo** , non siano negativi.

</dd> <dt>

<span id="tools.e_14_gly"></span><span id="TOOLS.E_14_GLY"></span>**Prevista stringa in un'STRINGTABLE**
</dt> <dd>

È prevista una stringa dopo ogni parametro numerico *stringid* in un'istruzione [**un'STRINGTABLE**](stringtable-resource.md) .

</dd> <dt>

<span id="tools.e_15_gly"></span><span id="TOOLS.E_15_GLY"></span>**Prevista stringa o comando costante Accelerator**
</dt> <dd>

Il compilatore di risorse di Microsoft Windows (RC) non è riuscito a determinare la chiave configurata per l'acceleratore. Il parametro *Event* nell'istruzione [**Accelerators**](accelerators-resource.md) potrebbe non essere valido.

</dd> <dt>

<span id="tools.e_16_gly"></span><span id="TOOLS.E_16_GLY"></span>**È prevista una parola chiave VALUE, BLOCK o END.**
</dt> <dd>

La struttura [**VERSIONINFO**](versioninfo-resource.md) richiede una parola chiave **value**, **Block** o **end** .

</dd> <dt>

<span id="tools.e_17_gly"></span><span id="TOOLS.E_17_GLY"></span>**Previsto numero per ID**
</dt> <dd>

È previsto un numero per il parametro *ID* di un'istruzione di [**controllo**](control-control.md) nell'istruzione della [**finestra di dialogo**](dialog-resource.md) . Assicurarsi di disporre di un numero o di un'istruzione [**\# define**](-define.md) per l'identificatore del controllo.

</dd> <dt>

<span id="tools.e_18_gly"></span><span id="TOOLS.E_18_GLY"></span>**Prevista stringa tra virgolette per la chiave**
</dt> <dd>

La stringa chiave che segue la parola chiave **Block** o **value** deve essere racchiusa tra virgolette doppie.

</dd> <dt>

<span id="tools.e_19_gly"></span><span id="TOOLS.E_19_GLY"></span>**Prevista stringa tra virgolette nella classe della finestra di dialogo**
</dt> <dd>

Il parametro *Class* dell'istruzione [**Class**](class-statement.md) nell'istruzione [**Dialog**](dialog-resource.md) deve essere un numero intero o una stringa racchiusa tra virgolette doppie (").

</dd> <dt>

<span id="tools.e_20_gly"></span><span id="TOOLS.E_20_GLY"></span>**Prevista stringa tra virgolette nel titolo della finestra di dialogo**
</dt> <dd>

Il parametro *CaptionText* dell'istruzione [**Caption**](caption-statement.md) nell'istruzione [**Dialog**](dialog-resource.md) deve essere una stringa di caratteri racchiusa tra virgolette doppie (").

</dd> </dl>

 

 




