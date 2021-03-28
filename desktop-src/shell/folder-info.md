---
description: La sezione ottenere l'ID di una cartella ha illustrato due approcci per ottenere il puntatore di un oggetto spazio dei nomi a un elenco di identificatori di elemento (PIDL).
ms.assetid: c99a2f6c-3144-41ec-ad97-59a30bfec9ab
title: Ottenere informazioni sul contenuto di una cartella
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7eb26e9df28af4811e74f2878eebb7af9d5c92a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104993685"
---
# <a name="getting-information-about-the-contents-of-a-folder"></a>Ottenere informazioni sul contenuto di una cartella

La sezione [ottenere l'ID di una cartella ha](folder-id.md) illustrato due approcci per ottenere il puntatore di un oggetto spazio dei nomi a un elenco di identificatori di elemento (PIDL). Una domanda ovvia è: quando si dispone di un PIDL, cosa è possibile fare? Una domanda correlata è: cosa accade se nessuno dei due approcci funziona o è adatto per l'applicazione? La risposta a entrambe le domande richiede un esame più approfondito del modo in cui viene implementato lo spazio dei nomi. La chiave è l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

-   [Uso dell'interfaccia IShellFolder](#using-the-ishellfolder-interface)
-   [Enumerazione del contenuto di una cartella](#enumerating-the-contents-of-a-folder)
-   [Determinazione dei nomi visualizzati e delle altre proprietà](#determining-display-names-and-other-properties)
-   [Recupero di un puntatore all'interfaccia IShellFolder di una sottocartella](#getting-a-pointer-to-a-subfolders-ishellfolder-interface)
-   [Determinazione della cartella padre di un oggetto](#determining-an-objects-parent-folder)

## <a name="using-the-ishellfolder-interface"></a>Uso dell'interfaccia IShellFolder

In precedenza in questa documentazione, le cartelle dello spazio dei nomi venivano definite oggetti. Anche se, a questo punto, il termine è stato usato in modo separato, si tratta effettivamente di un vero e proprio senso. Ogni cartella dello spazio dei nomi è rappresentata da un oggetto Component Object Model (COM). Ogni oggetto Folder espone una serie di interfacce che possono essere utilizzate per un'ampia gamma di attività. Alcune interfacce facoltative potrebbero non essere esposte da tutte le cartelle. Tuttavia, tutte le cartelle devono esporre l'interfaccia di base, [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder).

Il primo passaggio nell'uso di un oggetto Folder consiste nel recuperare un puntatore alla relativa interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Oltre a fornire l'accesso alle altre interfacce dell'oggetto, **IShellFolder** espone un gruppo di metodi che gestiscono una serie di attività comuni, alcune delle quali sono descritte in questa sezione.

Per recuperare un puntatore all'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) di un oggetto spazio dei nomi, è prima necessario chiamare [**SHGetDesktopFolder**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder). Questa funzione restituisce un puntatore all'interfaccia **IShellFolder** della radice dello spazio dei nomi, il desktop. Dopo aver creato l'interfaccia **IShellFolder** del desktop, è possibile procedere in diversi modi.

Se si dispone già del PIDL della cartella a cui si è interessati, ad esempio chiamando [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation), è possibile recuperare la relativa interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) chiamando il metodo [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) del desktop. Se si dispone del percorso di un oggetto file system, è necessario innanzitutto ottenere il relativo PIDL chiamando il metodo [**IShellFolder::P arsedisplayname**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname) del desktop e quindi chiamare **IShellFolder:: BindToObject**. Se nessuno di questi approcci è applicabile, è possibile usare altri metodi **IShellFolder** per spostarsi nello spazio dei nomi. Per ulteriori informazioni, vedere [spostamento nello spazio dei nomi](navigate.md).

## <a name="enumerating-the-contents-of-a-folder"></a>Enumerazione del contenuto di una cartella

La prima cosa che si vuole fare con una cartella è individuare il contenuto. È necessario chiamare prima il metodo [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) della cartella. La cartella creerà un oggetto enumerazione OLE standard e restituirà l'interfaccia [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) . Questa interfaccia espone quattro metodi standard, ovvero [**Clone**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone), [**Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next), [**Reset**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset)e [**Skip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip), che possono essere usati per enumerare il contenuto della cartella.

La procedura di base per l'enumerazione del contenuto di una cartella è la seguente:

1.  Chiamare il metodo Folders [**IShellFolder:: EnumObjects**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects) per recuperare un puntatore all'interfaccia [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) dell'oggetto di enumerazione.
2.  Passare un PIDL non allocato a [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). Si occuperà **quindi** di allocare PIDL, ma l'applicazione deve deallocarla quando non è più necessaria. Quando restituisce **Next** , il PIDL conterrà solo l'ID elemento dell'oggetto e i caratteri **null** di terminazione. In altre parole, si tratta di un PIDL a un solo livello relativo alla cartella, non di un PIDL completo.
3.  Ripetere il passaggio 2 fino a quando [**successivo**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next) restituisce \_ false per indicare che tutti gli elementi sono stati enumerati.
4.  Chiamare **IEnumIDList:: Release** per rilasciare l'oggetto di enumerazione.

> [!Note]  
> È importante tenere traccia dell'uso di un PIDL completo o relativo. Alcune funzioni e metodi accetteranno uno dei due, mentre altri ne accetteranno solo uno o l'altro.

 

I restanti tre metodi [**IEnumIDList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist) ([**Reset**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-reset), [**Skip**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-skip)e [**Clone**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-clone)) sono utili se è necessario eseguire enumerazioni ripetute della cartella. Consentono di reimpostare l'enumerazione, ignorare uno o più oggetti e creare una copia dell'oggetto di enumerazione per conservarne lo stato.

## <a name="determining-display-names-and-other-properties"></a>Determinazione dei nomi visualizzati e delle altre proprietà

Dopo aver enumerato tutti i PIDL contenuti in una cartella, è possibile individuare il tipo di oggetti che rappresentano. L'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) fornisce una serie di metodi utili, due dei quali sono discussi qui. Altri metodi **IShellFolder** e altre interfacce di cartelle della shell verranno discusse più avanti.

Una delle proprietà più utili è il nome visualizzato dell'oggetto. Per recuperare il nome visualizzato di un oggetto, passare il relativo PIDL a [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof). Sebbene l'oggetto possa trovarsi in qualsiasi punto sotto la cartella padre nello spazio dei nomi, il relativo PIDL deve essere relativo alla cartella.

[**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) restituisce il nome visualizzato come parte di una struttura [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) . Poiché l'estrazione del nome visualizzato da una struttura **STRRET** può essere un po' complicata, la shell fornisce due funzioni che eseguono il processo per l'utente, [**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra) e [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa). Entrambe le funzioni accettano una struttura **STRRET** e restituiscono il nome visualizzato come stringa normale. Si differenziano solo per la modalità di allocazione della stringa.

Oltre al nome visualizzato, un oggetto può avere diversi attributi, ad esempio se si tratta di una cartella o se può essere spostata. È possibile recuperare gli attributi di un oggetto passandone il PIDL a [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof). L'elenco completo degli attributi è molto grande, pertanto dovrebbe essere visualizzato il riferimento per i dettagli. Si noti che il PIDL passato a **GetAttributesOf** deve essere a livello singolo. In particolare, **IShellFolder:: GetAttributesOf** accetterà il PIDL restituito da [**IEnumIDList:: Next**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ienumidlist-next). È possibile passare una matrice di PIDL e **GetAttributesOf** restituirà gli attributi in comune per tutti gli oggetti nella matrice.

Se il percorso completo di un oggetto è PIDL, [**SHGetFileInfo**](/windows/desktop/api/Shellapi/nf-shellapi-shgetfileinfoa) fornisce un modo semplice per recuperare informazioni su un oggetto sufficiente per molti scopi. **SHGetFileInfo** accetta un percorso completo o PIDL e restituisce una serie di informazioni sull'oggetto, tra cui:

-   Nome visualizzato dell'oggetto
-   Attributi dell'oggetto
-   Handle per le icone dell'oggetto
-   Handle per l'elenco di immagini di sistema
-   Percorso del file contenente l'icona dell'oggetto.

## <a name="getting-a-pointer-to-a-subfolders-ishellfolder-interface"></a>Recupero di un puntatore all'interfaccia IShellFolder di una sottocartella

È possibile determinare se la cartella contiene sottocartelle chiamando [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof) e verificando se \_ è impostato il flag di cartella SFGAO. Se un oggetto è una cartella, è possibile associarlo, che fornisce un puntatore alla relativa interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) .

Per eseguire l'associazione a una sottocartella, chiamare il metodo [**IShellFolder:: BindToObject**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-bindtoobject) della cartella padre. Questo metodo accetta il PIDL della sottocartella e restituisce un puntatore alla relativa interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) . Una volta ottenuto questo puntatore, è possibile utilizzare i metodi **IShellFolder** per enumerare il contenuto delle sottocartelle, determinarne le proprietà e così via.

## <a name="determining-an-objects-parent-folder"></a>Determinazione della cartella padre di un oggetto

Se si dispone di un PIDL di un oggetto, potrebbe essere necessario un handle per una delle interfacce esposte dalla relativa cartella padre. Se ad esempio si desidera determinare il nome visualizzato associato a un PIDL tramite [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof), è necessario recuperare prima l'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) dell'elemento padre dell'oggetto. È possibile eseguire questa operazione con le tecniche descritte nelle sezioni precedenti. Tuttavia, un approccio molto più semplice consiste nell'usare la funzione Shell [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent). Questa funzione accetta l'PIDL completo di un oggetto e restituisce un puntatore a interfaccia specificato nella cartella padre. Facoltativamente, restituisce anche il PIDL a singolo livello dell'elemento per l'uso in metodi quali [**IShellFolder:: GetAttributesOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof).

Nell'applicazione console di esempio seguente viene recuperato il PIDL della cartella speciale di sistema e viene restituito il relativo nome visualizzato.


```
#include <shlobj.h>
#include <shlwapi.h>
#include <iostream.h>
#include <objbase.h>

int main()
{
    IShellFolder *psfParent = NULL;
    LPITEMIDLIST pidlSystem = NULL;
    LPCITEMIDLIST pidlRelative = NULL;
    STRRET strDispName;
    TCHAR szDisplayName[MAX_PATH];
    HRESULT hr;

    hr = SHGetFolderLocation(NULL, CSIDL_SYSTEM, NULL, NULL, &pidlSystem);

    hr = SHBindToParent(pidlSystem, IID_IShellFolder, (void **) &psfParent, &pidlRelative);

    if(SUCCEEDED(hr))
    {
        hr = psfParent->GetDisplayNameOf(pidlRelative, SHGDN_NORMAL, &strDispName);
        hr = StrRetToBuf(&strDispName, pidlSystem, szDisplayName, sizeof(szDisplayName));
        cout << "SHGDN_NORMAL - " <<szDisplayName << '\n';
    }

    psfParent->Release();
    CoTaskMemFree(pidlSystem);

    return 0;
}
```



L'applicazione usa prima di tutto [**SHGetFolderLocation**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetfolderlocation) per recuperare il PIDL della cartella di sistema. Chiama quindi [**SHBindToParent**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shbindtoparent), che restituisce un puntatore all'interfaccia [**IShellFolder**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) della cartella padre e il PIDL della cartella di sistema rispetto al relativo elemento padre. USA quindi il metodo [**IShellFolder:: GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) della cartella padre per recuperare il nome visualizzato della cartella di sistema. Poiché **GetDisplayNameOf** restituisce una struttura [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret) , [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa) viene utilizzato per convertire il nome visualizzato in una stringa normale. Dopo aver visualizzato il nome visualizzato, i puntatori di interfaccia vengono rilasciati e il PIDL di sistema viene liberato. Si noti che non è necessario liberare il PIDL relativo restituito da **SHBindToParent**.

 

 
