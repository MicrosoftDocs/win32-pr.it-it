---
description: Questa sezione descrive come determinare la versione delle DLL della shell in cui è in esecuzione l'applicazione e come specificare come destinazione l'applicazione per una versione specifica.
title: 'Versioni delle DLL di shell e Shlwapi '
ms.topic: article
ms.date: 09/24/2020
ms.assetid: ecfb6484-a1d6-4ace-8457-3940b111a4d2
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6d74371478b30037e75b1c168dc235735ba6bd219fa461245262ff55a508ae5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967836"
---
# <a name="shell-and-shlwapi-dll-versions"></a>Versioni delle DLL di shell e Shlwapi 

Questa sezione descrive come determinare la versione delle DLL della shell in cui è in esecuzione l'applicazione e come specificare come destinazione l'applicazione per una versione specifica.

-   [Numeri di versione DLL](#dll-version-numbers)
-   [Uso di DllGetVersion per determinare il numero di versione](#using-dllgetversion-to-determine-the-version-number)
    -   [Uso di DllGetVersion](#using-dllgetversion)
-   [Project Versioni](#project-versions)

## <a name="dll-version-numbers"></a>Numeri di versione DLL

Tutti gli elementi di programmazione illustrati nella documentazione della shell sono contenuti in due DLL: Shell32.dll e Shlwapi.dll. Grazie ai miglioramenti in corso, diverse versioni di queste DLL implementano funzionalità diverse. In tutta la documentazione di riferimento della shell, ogni elemento di programmazione specifica un numero minimo di versione dll supportato. Questo numero di versione indica che l'elemento di programmazione viene implementato in tale versione e nelle versioni successive della DLL, se non diversamente specificato. Se non viene specificato alcun numero di versione, l'elemento di programmazione viene implementato in tutte le versioni esistenti della DLL.

Prima Windows XP, le nuove Shell32.dll e Shlwapi.dll venivano talvolta fornite con nuove versioni di Windows Internet Explorer. A Windows XP, tali DLL non venivano più fornite come file ridistribuibili al di fuori delle nuove versioni di Windows stesso. La tabella seguente illustra le diverse versioni delle DLL e come sono state distribuite a Microsoft Internet Explorer 3.0, Windows 95 e Microsoft Windows NT 4.0.

Shell32.dll versione 4.0 è disponibile nelle versioni originali di Windows 95 e Microsoft Windows NT 4.0. La shell non è stata aggiornata con la versione Internet Explorer 3.0, quindi Shell32.dll non ha una versione 4.70. Shell32.dll versioni 4.71 e 4.72 sono state fornite con le versioni Internet Explorer corrispondenti, ma non sono state necessariamente installate (vedere la nota 1). Per le versioni successive a Microsoft Internet Explorer 4.01 e Windows 98, i numeri di versione per Shell32.dll e Shlwapi.dll divergono. In generale, è consigliabile presupporre che le DLL presentino numeri di versione diversi e testare ognuna separatamente.

#### <a name="shell32dll"></a>Shell32.dll

| Versione | Piattaforma di distribuzione                                                       |
|---------|-----------------------------------------------------------------------------|
| 4.0     | Windows 95 e Microsoft Windows NT 4.0                                     |
| 4.71    | Microsoft Internet Explorer 4.0. Vedere la nota 1.                                |
| 4.72    | Internet Explorer 4.01 e Windows 98. Vedere la nota 1.                          |
| 5.0     | Windows 2000 e Windows Millennium Edition (Windows Me). Vedere la nota 2.       |
| 6.0     | Windows XP                                                                  |
| 6.0.1   | Windows Vista                                                               |
| 6.1     | Windows 7                                                                   |

#### <a name="shlwapidll"></a>Shlwapi.dll

| Versione | Piattaforma di distribuzione                                                       |
|---------|-----------------------------------------------------------------------------|
| 4.0     | Windows 95 e Microsoft Windows NT 4.0                                     |
| 4.71    | Internet Explorer 4.0. Vedere la nota 1.                                          |
| 4.72    | Internet Explorer 4.01 e Windows 98. Vedere la nota 1.                          |
| 4.7     | Internet Explorer 3.x                                                       |
| 5.0     | Microsoft Internet Explorer 5 e Windows 98 edizione Standard. Vedere la nota 2.                |
| 5.5     | Microsoft Internet Explorer 5.5 e Windows Millennium Edition (Windows Me) |
| 6.0     | Windows XP e Windows Vista                                                |



**Nota 1:** Tutti i sistemi con Internet Explorer 4.0 o 4.01 hanno la versione associata di Shlwapi.dll (4.71 o 4.72, rispettivamente). Tuttavia, per i sistemi precedenti Windows 98, Internet Explorer 4.0 e 4.01 possono essere installati con o senza la *shell integrata* di . Se Internet Explorer è stato installato con la shell integrata, è stata installata anche la versione associata di Shell32.dll (4.71 o 4.72). Se Internet Explorer è stato installato senza la shell integrata, Shell32.dll è rimasto come versione 4.0. In altre parole, la presenza della versione 4.71 o 4.72 di Shlwapi.dll in un sistema non garantisce che Shell32.dll abbia lo stesso numero di versione. Tutti Windows 98 sistemi hanno la versione 4.72 di Shell32.dll.

**Nota 2:** La versione 5.0 di Shlwapi.dll è stata distribuita con Internet Explorer 5 ed è stata trovata in tutti i sistemi in cui è stato installato Internet Explorer 5, ad eccezione di Windows 2000. La versione 5.0 di Shell32.dll è stata distribuita in modo nativo con Windows 2000 e Windows Millennium Edition (Windows Me), insieme alla versione 5.0 di Shlwapi.dll.

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Uso di DllGetVersion per determinare il numero di versione

A partire dalla versione 4.71, le DLL della shell, tra le altre, hanno iniziato a esportare [**DllGetVersion.**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) Questa funzione può essere chiamata da un'applicazione per determinare quale versione della DLL è presente nel sistema.

> [!Note]  
> Le DLL non esportano necessariamente [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc). Eseguire sempre il test prima di provare a usarlo.

Per Windows precedenti a Windows 2000, [**DllGetVersion**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) restituisce una struttura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) che contiene i numeri di versione principale e secondaria, il numero di build e un ID piattaforma. Per Windows 2000 e versioni successive, **DllGetVersion** potrebbe restituire invece una [**struttura DLLVERSIONINFO2.**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) Oltre alle informazioni fornite tramite **DLLVERSIONINFO,** **DLLVERSIONINFO2** fornisce anche il numero di hotfix che identifica il Service Pack installato più recente, che offre un modo più affidabile per confrontare i numeri di versione. Poiché il primo membro di **DLLVERSIONINFO2 è** una **struttura DLLVERSIONINFO,** la struttura successiva è compatibile con le versioni precedenti.

### <a name="using-dllgetversion"></a>Uso di DllGetVersion

La funzione di esempio `GetVersion` seguente carica una DLL specificata e tenta di chiamare la relativa funzione [**DllGetVersion.**](/windows/desktop/api/Shlwapi/nc-shlwapi-dllgetversionproc) Se ha esito positivo, usa una macro per creare un pacchetto dei numeri di versione principale e secondario dalla struttura [**DLLVERSIONINFO**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo) in un **valore DWORD** restituito all'applicazione chiamante. Se la DLL non esporta **DllGetVersion**, la funzione restituisce zero. Con Windows 2000 e versioni successive, è possibile modificare la funzione per gestire la possibilità che **DllGetVersion** restituisca una [**struttura DLLVERSIONINFO2.**](/windows/desktop/api/Shlwapi/ns-shlwapi-dllversioninfo2) In tal caso, usare le informazioni contenute nel membro **ullVersion** della struttura **DLLVERSIONINFO2** per confrontare versioni, numeri di build e versioni del Service Pack. La macro [**MAKEDLLVERULL**](/windows/desktop/api/Shlwapi/nf-shlwapi-makedllverull) semplifica l'attività di confronto di questi valori con quelli in **ullVersion.**

> [!Note]  
> [**L'uso errato di LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) può comportare rischi per la sicurezza. Per informazioni su come caricare correttamente le DLL con versioni diverse di Windows, vedere la documentazione di **LoadLibrary.**


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    /* For security purposes, LoadLibrary should be provided with a fully qualified 
       path to the DLL. The lpszDllName variable should be tested to ensure that it 
       is a fully qualified path before it is used. */
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        /* Because some DLLs might not implement this function, you must test for 
           it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
           function can be a useful indicator of the version. */

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```


Nell'esempio di codice seguente viene illustrato come utilizzare per verificare se Shell32.dll `GetVersion` versione è 6.0 o successiva.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\Shell32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of Shell32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```


## <a name="project-versions"></a>Project Versioni

Per garantire che l'applicazione sia compatibile con versioni di destinazione diverse di un file .dll, nei file di intestazione sono presenti macro di versione. Queste macro vengono usate per definire, escludere o ridefinire determinate definizioni per versioni diverse della DLL. Per [una descrizione dettagliata di queste macro, vedere](../winprog/using-the-windows-headers.md) Using the Windows Headers (Uso delle intestazioni dei dati).

Ad esempio, il nome della macro **\_ WIN32 \_ IE** si trova comunemente nelle intestazioni precedenti. L'utente è responsabile della definizione della macro come numero esadecimale. Questo numero di versione definisce la versione di destinazione dell'applicazione che utilizza la DLL. La tabella seguente mostra i numeri di versione disponibili e l'effetto di ognuno sull'applicazione.


| Versione | Descrizione                                                                                                                                                                                       |
|---------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0200  | L'applicazione è compatibile con Shell32.dll versione 4.00 e successive. L'applicazione non può implementare funzionalità aggiunte dopo la versione 4.00.                                              |
| 0x0300  | L'applicazione è compatibile con Shell32.dll versione 4.70 e successive. L'applicazione non può implementare funzionalità aggiunte dopo la versione 4.70.                                              |
| 0x0400  | L'applicazione è compatibile con Shell32.dll versione 4.71 e successive. L'applicazione non può implementare funzionalità aggiunte dopo la versione 4.71.                                              |
| 0x0401  | L'applicazione è compatibile con Shell32.dll versione 4.72 e successive. L'applicazione non può implementare funzionalità aggiunte dopo la versione 4.72.                                              |
| 0x0500  | L'applicazione è compatibile con Shell32.dll e Shlwapi.dll versione 5.0 e successive. L'applicazione non può implementare funzionalità aggiunte dopo la versione 5.0 di Shell32.dll e Shlwapi.dll. |
| 0x0501  | L'applicazione è compatibile con Shell32.dll e Shlwapi.dll versione 5.0 e successive. L'applicazione non può implementare funzionalità aggiunte dopo la versione 5.0 di Shell32.dll e Shlwapi.dll. |
| 0x0600  | L'applicazione è compatibile con Shell32.dll e Shlwapi.dll versione 6.0 e successive. L'applicazione non può implementare funzionalità aggiunte dopo la versione 6.0 di Shell32.dll e Shlwapi.dll. |


Se non si definisce la macro di **\_ \_ IE WIN32** nel progetto, questa viene definita automaticamente come 0x0500. Per definire un valore diverso, è possibile aggiungere quanto segue alle direttive del compilatore nel file make. sostituire il numero di versione desiderato per 0x0400.

```
/D _WIN32_IE=0x0400
```

Un altro metodo è aggiungere una riga simile alla seguente nel codice sorgente prima di includere i file di intestazione della shell. Sostituire il numero di versione desiderato 0x0400.

```
#define _WIN32_IE 0x0400
#include <commctrl.h>
```
