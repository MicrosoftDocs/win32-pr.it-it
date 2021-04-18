---
title: Informazioni del registro di sistema controlli ActiveX
description: Informazioni del registro di sistema controlli ActiveX
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b6b180b327a4239b220185a9073ebc7bc0826c39
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104517139"
---
# <a name="activex-controls-registry-information"></a>Informazioni del registro di sistema controlli ActiveX

Sono disponibili diverse voci del registro di sistema e flag utilizzati. Inoltre, i controlli possono supportare le categorie di componenti per classificare le funzionalità che forniscono.

Le chiavi del registro di sistema correlate ai controlli sono contrassegnate con un asterisco nell'albero seguente:

```
HKEY_CLASSES_ROOT
   CLSID
      {control_CLSID}
         ProgID = <identifier>
         InprocServer32 = <filename>.dll
         *DefaultIcon = <filename>.<ext>,resourceID
         *ToolboxBitmap32 = <filename>.<ext>,resourceID
         *Control
         verb
            *n = &Properties...
         *MiscStatus = 0
         TypeLib = {object_typelibID}
         *Version = version_number
```

La voce **DefaultIcon** viene utilizzata per identificare un'icona da visualizzare quando il controllo è ridotto a icona. La funzione [**ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) viene usata per ottenere l'icona da. DLL o. File EXE specificato.

La voce **ToolboxBitmap32** identifica il nome del modulo e l'identificatore di risorsa per una \* bitmap di 16 15 da usare per la superficie di una barra degli strumenti o un pulsante della casella degli strumenti. Le dimensioni dell'icona standard di Windows sono troppo grandi per essere usate a questo scopo. Questa voce supporta in modo specifico i contenitori di controllo che dispongono di una modalità di progettazione in cui uno seleziona i controlli e li inserisce in un modulo progettato. In Visual Basic, ad esempio, l'icona del controllo viene visualizzata nella casella degli strumenti Visual Basic durante la modalità progettazione.

La voce di **controllo** contrassegna un oggetto come controllo. Questa voce viene spesso usata dai contenitori per compilare le finestre di dialogo. Il contenitore usa questa sottochiave per determinare se includere un oggetto in una finestra di dialogo in cui sono visualizzati i controlli.

La chiave secondaria **inseribile** può essere usata anche con i controlli, a seconda che l'oggetto possa agire solo come oggetto incorporato sul posto senza funzionalità di controllo speciali. Gli oggetti contrassegnati con **Insertable** vengono visualizzati nella finestra di dialogo Inserisci oggetto del relativo contenitore. La voce **Insertable** indica in genere che il controllo è stato testato con contenitori non di controllo.

I sottochiavi **Insertable** e **Control** sono facoltativi. Un controllo può omettere la sottochiave **inseribile** se non è progettata per funzionare con i contenitori meno recenti che non comprendono i controlli. Un controllo può omettere la chiave del **controllo** se è progettata solo per funzionare con un contenitore specifico e pertanto non vuole essere inserita in altri contenitori.

I controlli devono avere un verbo Properties, \_ le proprietà OLEIVERB, insieme a tutti gli altri verbi supportati. Il verbo Properties, così come il verbo standard OLEIVERB \_ Primary, indica al controllo di visualizzare la relativa finestra delle proprietà. Il verbo Properties viene visualizzato come elemento Properties nel menu del contenitore quando il controllo è attivo. In questo modo, il controllo può visualizzare la propria pagina delle proprietà che consente alcune funzionalità utili all'utente finale, anche se il contenitore non gestisce i controlli.

Un controllo definisce la chiave **miscStatus** per la descrizione di contenitori potenziali. I bit accettano i valori di [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)e i controlli aggiungono diversi valori a questa enumerazione. Per ulteriori informazioni, vedere i valori di enumerazione **OLEMISC** . Il client può ottenere queste informazioni chiamando [**IOleObject:: GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) senza dover creare prima un'istanza del controllo.

Infine, **Version** descrive la versione del controllo che deve corrispondere alla versione della libreria dei tipi associata a questo controllo.

Inoltre, nelle informazioni sul tipo per un controllo, il controllo attributo contrassegna una voce della coclasse come descrizione di un controllo.

 

 