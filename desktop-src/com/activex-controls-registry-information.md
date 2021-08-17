---
title: ActiveX Controlla le informazioni del Registro di sistema
description: ActiveX Controlla le informazioni del Registro di sistema
ms.assetid: fda5b1e6-2048-4df7-ba8f-145652e3883c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87f062c11304c50161308cc5c6e43001c23f63486e60e568f61d6335f0947380
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737385"
---
# <a name="activex-controls-registry-information"></a>ActiveX Controlla le informazioni del Registro di sistema

Sono disponibili una serie di voci e flag del Registro di sistema usati. Inoltre, i controlli possono supportare le categorie di componenti per classificare le funzionalità fornite.

Le chiavi del Registro di sistema correlate ai controlli sono contrassegnate con un asterisco nell'albero seguente:

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

La **voce DefaultIcon** viene usata per identificare un'icona da visualizzare quando il controllo viene ridotto a icona. La [**funzione ExtractIcon**](/windows/win32/api/shellapi/nf-shellapi-extracticona) viene usata per ottenere l'icona dal .DLL o .EXE file specificato.

La **voce ToolboxBitmap32** identifica il nome del modulo e l'identificatore di risorsa per una bitmap da 16 15 da usare per il viso di una barra degli strumenti o di un pulsante \* della casella degli strumenti. Le dimensioni Windows'icona standard sono troppo grandi per essere usate a questo scopo. Questa voce supporta in modo specifico i contenitori di controlli con una modalità di progettazione in cui si selezionano i controlli e li inserisce in un form in fase di progettazione. Ad esempio, in Visual Basic, l'icona del controllo viene visualizzata nella casella degli strumenti Visual Basic durante la modalità progettazione.

La **voce Control** contrassegna un oggetto come controllo . Questa voce viene spesso usata dai contenitori per compilare le finestre di dialogo. Il contenitore usa questa sottochiave per determinare se includere un oggetto in una finestra di dialogo che visualizza i controlli.

La **sotto-chiave** inseribile può essere usata anche con i controlli , a seconda che l'oggetto possa fungere solo da oggetto incorporato sul posto senza funzionalità di controllo speciali. Gli oggetti contrassegnati **con Inseriscibile** vengono visualizzati nella finestra di dialogo Inserisci oggetto del contenitore. La **voce Inseriscibile** in genere indica che il controllo è stato testato con contenitori non di controllo.

Entrambe **le sottochiavi Insertable** **e Control** sono facoltative. Un controllo può omettere la sottochiave **Inseriscibile** se non è progettato per funzionare con contenitori meno recenti che non comprendono i controlli. Un controllo può omettere il **tasto Control** se è progettato solo per funzionare con un contenitore specifico e pertanto non vuole essere inserito in altri contenitori.

I controlli devono avere un verbo Properties, OLEIVERB \_ PROPERTIES, insieme a qualsiasi altro verbo che supportano. Il verbo Properties, nonché il verbo standard OLEIVERB PRIMARY, indica al controllo di \_ visualizzare la relativa finestra delle proprietà. Il verbo Properties viene visualizzato come elemento Properties nel menu del contenitore quando il controllo è attivo. In questo modo, il controllo può visualizzare la propria pagina delle proprietà consentendo alcune funzionalità utili all'utente finale, anche se il contenitore non gestisce i controlli.

Un controllo definisce la chiave **MiscStatus** per descriversi in potenziali contenitori. I bit accettano i valori di [**OLEMISC**](/windows/win32/api/oleidl/ne-oleidl-olemisc)e i controlli aggiungono diversi valori a questa enumerazione. Per altre informazioni, vedere i valori di enumerazione **OLEMISC.** Il client può ottenere queste informazioni chiamando [**IOleObject::GetMiscStatus**](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getmiscstatus) senza dover prima creare un'istanza del controllo.

Infine, **Version** descrive la versione del controllo che deve corrispondere alla versione della libreria dei tipi associata a questo controllo.

Anche nelle informazioni sul tipo per un controllo, il controllo attributo contrassegna una voce di coclasse come descrizione di un controllo.

 

 