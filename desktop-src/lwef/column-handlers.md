---
title: Creazione di gestori di colonne
description: La visualizzazione Dettagli in Windows Windows Explorer visualizza in genere diverse colonne standard.
ms.assetid: 805e0e13-d09e-40f8-955b-c585f388e07e
keywords:
- gestori di colonne
- register,column handlers
- Getcolumninfo
- GetItemData
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90876aecdb2626326513723f0cd2c5a6e8f66bfd938b3f56cf10bd3624dd8687
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119349463"
---
# <a name="creating-column-handlers"></a>Creazione di gestori di colonne

\[Questa funzionalità è supportata solo in Windows XP o versioni precedenti. \]

La visualizzazione Dettagli in Windows Windows Explorer visualizza in genere diverse colonne standard. Ogni colonna elenca le informazioni, ad esempio le dimensioni o il tipo di file, per ogni file nella cartella corrente. Implementando e registrando un gestore colonne, è possibile rendere le colonne personalizzate disponibili per la visualizzazione.

Le procedure generali per l'implementazione e la registrazione di un gestore estensioni della shell sono descritte in [Creazione di gestori di estensioni della shell.](/windows/desktop/shell/handlers) Questo documento è in particolare sugli aspetti dell'implementazione specifici dei gestori di colonne.

Vengono illustrati gli argomenti seguenti.

-   [Funzionamento dei gestori di colonne](#how-column-handlers-work)
-   [Registrazione di gestori di colonne](#registering-column-handlers)
-   [Implementazione di gestori di colonne](#implementing-column-handlers)
    -   [Metodo Initialize](#the-initialize-method)
    -   [Metodo GetColumnInfo](#the-getcolumninfo-method)
    -   [Metodo GetItemData](#the-getitemdata-method)

## <a name="how-column-handlers-work"></a>Funzionamento dei gestori di colonne

La figura seguente mostra Windows Explorer nella visualizzazione Dettagli.

![Screenshot di Esplora risorse nella visualizzazione dettagli](images/columnproviderhandler1.jpg)

Con Windows 2000, la cartella può supportare anche alcune colonne che, per impostazione predefinita, non vengono visualizzate. L'utente può visualizzare colonne aggiuntive facendo clic con  il pulsante destro del mouse su una delle intestazioni di colonna e selezionando il comando Altro dal menu. Viene quindi visualizzata una finestra di dialogo che elenca le colonne disponibili per la cartella e consente all'utente di selezionare le colonne da visualizzare. Nella figura seguente viene illustrata questa finestra di dialogo per l'esempio precedente.

![Screenshot di Esplora risorse con la finestra di dialogo Scegli dettagli visualizzata](images/columnproviderhandler2.jpg)

Creando un gestore colonne, è possibile creare colonne personalizzate e aggiungerle a tale elenco. Ad esempio, una raccolta di file che contengono musica potrebbe usare un gestore colonne per visualizzare le colonne che elencano l'artista e la parte contenuta in ogni file.

Un gestore di colonna è un oggetto globale che viene chiamato ogni volta che Windows Explorer visualizza la visualizzazione Dettagli. Tuttavia, i gestori di colonne vengono in genere utilizzati per visualizzare colonne personalizzate solo per i membri di un particolare [tipo di file](/windows/desktop/shell/fa-file-types). Prima di visualizzare la visualizzazione Dettagli, Windows Explorer esegue una query su tutti i gestori di colonne registrati per le relative caratteristiche di colonna. Se l'utente ha selezionato una delle colonne del gestore, Windows Explorer esegue una query sul gestore per i dati associati. Quando un gestore di colonne riceve una richiesta di dati, la fornisce se il file è un membro del tipo supportato. In caso contrario, ignora la richiesta restituisce S \_ FALSE.

## <a name="registering-column-handlers"></a>Registrazione di gestori di colonne

I gestori di colonna vengono registrati nella sottochiave seguente.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
```

Creare una sottochiave di **ColumnHandlers** denominata con il formato stringa del GUID dell'identificatore di classe (CLSID) del gestore. Per una descrizione generale di come registrare i gestori di estensioni della shell, vedere [Creazione di gestori di estensioni della shell.](/windows/desktop/shell/handlers) Nell'esempio seguente viene illustrato come registrare un gestore di colonna.

```
HKEY_CLASSES_ROOT
   Folder
      shellex
         ColumnHandlers
            {My Column Handler CLSID GUID}
```

## <a name="implementing-column-handlers"></a>Implementazione di gestori di colonne

Come tutti i gestori di estensioni della shell, i gestori di colonne sono oggetti COM (In-Process Component Object Model) implementati come DLL. Esportano [**l'interfaccia IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) oltre a [IUnknown.](/windows/win32/api/unknwn/nn-unknwn-iunknown)

Windows Explorer chiama i tre metodi esportati da [**IColumnProvider**](/windows/desktop/api/shlobj/nn-shlobj-icolumnprovider) per richiedere le informazioni necessarie per visualizzare la colonna. La procedura usata da Windows Explorer è la seguente:

1.  Chiamare [**IColumnProvider::Initialize**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) per specificare la cartella che sta per essere visualizzata.
2.  Chiamare [**IColumnProvider::GetColumnInfo per**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) recuperare l'identificatore e le caratteristiche della colonna.
3.  Se la colonna è stata selezionata dall'utente, chiamare [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) per ogni file nella cartella per recuperare i dati che appartengono alla voce di colonna del file.

### <a name="the-initialize-method"></a>Metodo Initialize

Windows Explorer chiama [**IColumnProvider::Initialize per**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-initialize) inizializzare il gestore di colonne. Il metodo ha tre parametri, ma attualmente viene usato solo *wszFolder.* È impostato sulla cartella la cui visualizzazione Dettagli sta per essere visualizzata. Archiviare il nome della cartella per usarlo in seguito e inizializzare l'oggetto gestore in base alle esigenze.

### <a name="the-getcolumninfo-method"></a>Metodo GetColumnInfo

Windows Explorer chiama quindi [**IColumnProvider::GetColumnInfo**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getcolumninfo) per richiedere l'identificatore e le caratteristiche della colonna. Passa un indice per la colonna nel *parametro dwIndex.* Questo indice è un valore arbitrario utilizzato per enumerare le colonne. Windows Explorer passa anche un puntatore a [**una struttura SHCOLUMNINFO.**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) Questa struttura viene utilizzata per restituire l'identificatore e le caratteristiche della colonna. **IColumnProvider::GetColumnInfo deve** assegnare i valori appropriati ai membri della struttura e restituire .

Le colonne sono identificate dall'ID del set di proprietà OLE (FMTID) e da un ID di proprietà (PID) associato. Il primo membro della [**struttura SHCOLUMNINFO,**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) **scid**, è un puntatore a [**una struttura SHCOLUMNID**](/windows/desktop/shell/objects) usata per identificare la colonna. Il **relativo membro fmtid** contiene fmTID della colonna e il relativo **membro pid** contiene il PID della colonna. Ad esempio, una coppia standard FMTID/PID comunemente usata per identificare le colonne è il PID autore del set di proprietà Informazioni di riepilogo.

Se possibile, il gestore deve usare FMTID e PIN esistenti per identificare la colonna che supporta. Se si usa una [**struttura SHCOLUMNID**](/windows/desktop/shell/objects) personalizzata, la colonna visualizza i dati solo per i file supportati dal gestore. Se la cartella contiene altri file, le relative voci saranno vuote. Se una cartella contiene file di più di un tipo di file, l'uso di valori FMTID/PID standard potrebbe rendere possibile l'unione di dati di tipi diversi nella stessa colonna.

Impostare il **membro vt** sul [**tipo VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) dei dati da visualizzare nella colonna. Il tipo più comunemente usato è VT LPSTR, perché la maggior parte delle colonne \_ visualizza i dati come stringhe di caratteri. I membri rimanenti della [**struttura SHCOLUMNINFO**](/windows/desktop/api/shlobj/ns-shlobj-shcolumninfo) vengono usati per definire le caratteristiche della colonna. Assegnare i valori in base alle esigenze.

### <a name="the-getitemdata-method"></a>Metodo GetItemData

Se la colonna del gestore colonne è stata selezionata, Windows Explorer chiama [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) per ogni file nella cartella da visualizzare. Il *parametro pscid* è un puntatore a una [**struttura SHCOLUMNID**](/windows/desktop/shell/objects) che identifica la colonna. Il *parametro pscd* punta a una [**struttura SHCOLUMNDATA**](/windows/desktop/api/shlobj/ns-shlobj-shcolumndata) che identifica il file specifico.

Il *parametro pvarData* restituisce i dati che devono essere visualizzati nella colonna del gestore per il file specificato da *pscd*. Se il file è supportato dal gestore di colonne, assegnare il relativo valore di dati a *pvarData* e restituire S \_ OK. Se il file non è supportato dal gestore di colonne, restituire S \_ FALSE senza assegnare un valore a *pvarData*.

Molte cartelle conterranno una serie di file che non sono supportati da un gestore colonne specifico. Per migliorare l'efficienza, [**IColumnProvider::GetItemData**](/windows/desktop/api/shlobj/nf-shlobj-icolumnprovider-getitemdata) deve prima controllare il membro **pwszExt** della struttura a cui punta *pscd*. Questo membro contiene l'estensione del nome file. Se l'estensione indica che il file non è un membro di un tipo di file supportato dal gestore, evitare l'elaborazione non necessaria con la restituzione immediata di S \_ FALSE.

 

 