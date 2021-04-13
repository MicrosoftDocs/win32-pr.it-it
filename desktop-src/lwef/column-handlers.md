---
title: Creazione di gestori di colonne
description: Nella visualizzazione dettagli di Esplora risorse di Windows vengono normalmente visualizzate diverse colonne standard.
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- gestori colonne
- Register, gestori colonne
- GetColumnInfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 940796e75f29ba0fcfa025d9a56267e14bdff38f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104555476"
---
# <a name="creating-column-handlers"></a>Creazione di gestori di colonne

\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti. \]

Nella visualizzazione dettagli di Esplora risorse di Windows vengono normalmente visualizzate diverse colonne standard. Ogni colonna elenca le informazioni, ad esempio le dimensioni o il tipo di file, per ogni file nella cartella corrente. Implementando e registrando un gestore colonne, è possibile rendere disponibili colonne personalizzate per la visualizzazione.

Le procedure generali per l'implementazione e la registrazione di un gestore di estensione della shell sono descritte in [creazione di gestori di estensioni della shell](/windows/desktop/shell/handlers). Questo documento è incentrato sugli aspetti dell'implementazione specifici dei gestori di colonne.

Vengono illustrati gli argomenti seguenti.

-   [Funzionamento del gestore colonne](#how-column-handlers-work)
-   [Registrazione di gestori di colonne](#registering-column-handlers)
-   [Implementazione di gestori di colonne](#implementing-column-handlers)
    -   [Metodo Initialize](#the-initialize-method)
    -   [Metodo GetColumnInfo](#the-getcolumninfo-method)
    -   [Metodo GetItemData](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>Funzionamento del gestore colonne

Nella figura seguente viene illustrato Esplora risorse in visualizzazione dettagli.

![Screenshot di Esplora risorse in visualizzazione dettagli](images/columnproviderhandler1.jpg)

Con Windows 2000, la cartella può supportare anche un numero di colonne che, per impostazione predefinita, non vengono visualizzate. L'utente può visualizzare colonne aggiuntive facendo clic con il pulsante destro del mouse su una delle intestazioni di colonna e selezionando il comando **altro** nel menu. Viene visualizzata una finestra di dialogo in cui sono elencate le colonne disponibili per la cartella e si consente all'utente di selezionare le colonne da visualizzare. Nella figura seguente è illustrata questa finestra di dialogo per l'esempio precedente.

![Screenshot di Esplora risorse con la finestra di dialogo Seleziona dettagli visualizzata](images/columnproviderhandler2.jpg)

Creando un gestore colonne, è possibile creare colonne personalizzate e aggiungerle a tale elenco. Ad esempio, una raccolta di file che contengono musica può usare un gestore colonne per visualizzare le colonne che elencano l'artista e la parte contenuta da ogni file.

Un gestore colonne è un oggetto globale che viene chiamato ogni volta che Esplora risorse Visualizza la visualizzazione dettagli. I gestori di colonne, tuttavia, vengono in genere utilizzati per visualizzare colonne personalizzate solo per i membri di un determinato [tipo di file](/windows/desktop/shell/fa-file-types). Prima di visualizzare la visualizzazione dettagli, Esplora risorse esegue una query su tutti i gestori di colonne registrate per le relative caratteristiche di colonna. Se l'utente ha selezionato una delle colonne del gestore, Esplora risorse esegue una query sul gestore per i dati associati. Quando un gestore di colonne riceve una richiesta di dati, lo fornisce se il file è un membro del tipo supportato. In caso contrario, la richiesta viene ignorata restituendo S \_ false.

## <a name="registering-column-handlers"></a>Registrazione di gestori di colonne

I gestori di colonna vengono registrati nella sottochiave seguente.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

Creare una sottochiave di **ColumnHandlers** denominata con il formato stringa del GUID dell'identificatore di classe del gestore (CLSID). Per informazioni generali su come registrare i gestori di estensioni della shell, vedere [creazione di gestori di estensioni della shell](/windows/desktop/shell/handlers). Nell'esempio seguente viene illustrato come registrare un gestore colonne.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>Implementazione di gestori di colonne

Come tutti i gestori di estensioni della shell, i gestori di colonne sono oggetti COM (Component Object Model in-process) implementati come dll. Esportano l'interfaccia [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) oltre a [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

Esplora risorse chiama i tre metodi esportati da [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) per richiedere le informazioni necessarie per visualizzare la colonna. La procedura utilizzata da Esplora risorse è la seguente:

1.  Chiamare [**IColumnProvider:: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) per specificare la cartella che sta per essere visualizzata.
2.  Chiamare [**IColumnProvider:: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) per recuperare l'identificatore e le caratteristiche della colonna.
3.  Se la colonna è stata selezionata dall'utente, chiamare [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) per ogni file nella cartella per recuperare i dati che appartengono alla voce di colonna del file.

### <a name="the-initialize-method"></a>Metodo Initialize

Esplora risorse chiama [**IColumnProvider:: Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) per inizializzare il gestore colonne. Il metodo ha tre parametri, ma è attualmente in uso solo *wszFolder* . Viene impostato sulla cartella la cui visualizzazione dettagli sta per essere visualizzata. Archiviare il nome della cartella per utilizzarlo in un secondo momento e inizializzare l'oggetto gestore in base alle esigenze.

### <a name="the-getcolumninfo-method"></a>Metodo GetColumnInfo

In Esplora risorse viene chiamato [**IColumnProvider:: GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) per richiedere l'identificatore e le caratteristiche della colonna. Viene passato un indice per la colonna nel parametro *dwIndex* . Questo indice è un valore arbitrario utilizzato per enumerare colonne. Esplora risorse passa inoltre un puntatore a una struttura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) . Questa struttura viene utilizzata per restituire l'identificatore e le caratteristiche della colonna. **IColumnProvider:: GetColumnInfo** deve assegnare i valori appropriati ai membri della struttura e restituire.

Le colonne sono identificate dall'ID del set di proprietà OLE (FMTID) e da un ID di proprietà associato (PID). Il primo membro della struttura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) , **SCID**, è un puntatore a una struttura [**SHCOLUMNID**](/windows/desktop/shell/objects) utilizzata per identificare la colonna. Il membro **fmtid** include il fmtid della colonna e il relativo membro **PID** include il PID della colonna. Ad esempio, una coppia FMTID/PID standard comunemente utilizzata per identificare le colonne è il PID autore del set di proprietà informazioni di riepilogo.

Se possibile, il gestore deve usare FMTIDs e PID esistenti per identificare la colonna supportata. Se si utilizza una struttura [**SHCOLUMNID**](/windows/desktop/shell/objects) personalizzata, nella colonna verranno visualizzati i dati solo per i file supportati dal gestore. Se la cartella contiene altri file, le relative voci saranno vuote. Se una cartella contiene file di più di un tipo di file, l'utilizzo di valori FMTID/PID standard potrebbe consentire di unire i dati di tipi diversi nella stessa colonna.

Impostare il membro **VT** sul tipo [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant)   dei dati che si desidera visualizzare nella colonna. Il tipo usato più di frequente è VT \_ LPSTR, in quanto la maggior parte delle colonne Visualizza i dati come stringhe di caratteri. Gli altri membri della struttura [**SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) vengono utilizzati per definire le caratteristiche della colonna. Assegnare i valori nel modo appropriato.

### <a name="the-getitemdata-method"></a>Metodo GetItemData

Se è stata selezionata la colonna del gestore colonne, Esplora risorse chiama [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) per ogni file presente nella cartella da visualizzare. Il parametro *pscid* è un puntatore a una struttura [**SHCOLUMNID**](/windows/desktop/shell/objects) che identifica la colonna. Il parametro *PSCD* punta a una struttura [**SHCOLUMNDATA**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata) che identifica il file specifico.

Il parametro *pvarData* restituisce i dati che devono essere visualizzati nella colonna del gestore per il file specificato da *PSCD*. Se il file è supportato dal gestore colonne, assegnare il valore dei dati a *pvarData* e restituire S \_ OK. Se il file non è supportato dal gestore di colonne, restituire S \_ false senza assegnare un valore a *pvarData*.

Molte cartelle contengono un numero di file non supportati da alcun gestore di colonna specifico. Per migliorare l'efficienza, [**IColumnProvider:: GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) deve prima verificare il membro **pwszExt** della struttura a cui punta *PSCD*. Questo membro include l'estensione del nome file. Se l'estensione indica che il file non è un membro di un tipo di file supportato dal gestore, evitare l'elaborazione non necessaria restituendo immediatamente S \_ false.

 

 