---
title: Versioni di controllo comuni
description: Questo argomento elenca le versioni disponibili della libreria di controlli comuni (ComCtl32.dll), descrive come identificare la versione usata dall'applicazione e spiega come indirizzare l'applicazione per una versione specifica.
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc51fe027e6169ab1c28904c3145be2f5042d9a0
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 11/04/2020
ms.locfileid: "104474702"
---
# <a name="common-control-versions"></a>Versioni di controllo comuni

Questo argomento elenca le versioni disponibili della libreria di controlli comuni (ComCtl32.dll), descrive come identificare la versione usata dall'applicazione e spiega come indirizzare l'applicazione per una versione specifica.

In questo argomento sono contenute le sezioni seguenti.

-   [Numeri delle versioni DLL di controllo comuni](#common-control-dll-versions-numbers)
-   [Dimensioni della struttura per diverse versioni di controllo comuni](#structure-sizes-for-different-common-control-versions)
-   [Utilizzo di DllGetVersion per determinare il numero di versione](#using-dllgetversion-to-determine-the-version-number)
-   [Versioni del progetto](#project-versions)
-   [Argomenti correlati](#related-topics)

## <a name="common-control-dll-versions-numbers"></a>Numeri delle versioni DLL di controllo comuni

Il supporto per i controlli comuni è fornito da ComCtl32.dll, che tutte le versioni a 32 bit e a 64 bit di Windows includono. Ogni versione successiva della DLL supporta le funzionalità e le API delle versioni precedenti e aggiunge nuove funzionalità.

Poiché le diverse versioni di ComCtl32.dll sono state distribuite con Internet Explorer, la versione attiva è a volte diversa dalla versione fornita con il sistema operativo. Pertanto, l'applicazione deve determinare direttamente quale versione di ComCtl32.dll è presente.

Nella documentazione di riferimento dei controlli comuni, molti elementi di programmazione specificano un numero di versione di DLL minimo supportato. Questo numero di versione indica che l'elemento di programmazione viene implementato in tale versione e nelle versioni successive della DLL se non diversamente specificato. Se non viene specificato alcun numero di versione, l'elemento di programmazione viene implementato in tutte le versioni esistenti della DLL.

Nella tabella seguente vengono descritte le diverse versioni di DLL e il modo in cui sono state distribuite nei sistemi operativi supportati.



ComCtl32.dll

Versione

Piattaforma di distribuzione

5,81

Microsoft Internet Explorer 5,01, Microsoft Internet Explorer 5,5 e Microsoft Internet Explorer 6

5,82

Windows Server 2003, Windows Vista, Windows Server 2008 e Windows 7

6.0

Windows Server 2003

6.10

Windows Vista, Windows Server 2008 e Windows 7



 

## <a name="structure-sizes-for-different-common-control-versions"></a>Dimensioni della struttura per diverse versioni di controllo comuni

I miglioramenti continui apportati ai controlli comuni hanno comportato la necessità di estendere molte delle strutture. Per questo motivo, le dimensioni delle strutture sono cambiate tra le diverse versioni di COMmctrl. h. Poiché la maggior parte delle strutture di controllo comuni accetta una dimensione della struttura come uno dei parametri, un messaggio o una funzione può avere esito negativo se la dimensione non viene riconosciuta. Per ovviare a questo problema, sono state definite costanti di dimensione della struttura per facilitare la destinazione di una versione diversa di ComCtl32.dll. Nell'elenco seguente sono definite le costanti della dimensione della struttura.



|                               |                                                                                              |
|-------------------------------|----------------------------------------------------------------------------------------------|
| \_Dimensioni HDITEM V1 \_              | Dimensioni della struttura [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) nella versione 4,0.                           |
| \_Dimensioni IMAGELISTDRAWPARAMS V3 \_ | Dimensioni della struttura [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) nella versione 5,9. |
| \_Dimensioni LVCOLUMN V1 \_            | Dimensioni della struttura [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) nella versione 4,0.                       |
| \_Dimensioni LVGROUP V5 \_             | Dimensioni della struttura [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) nella versione 6,0.                         |
| \_Dimensioni LVHITTESTINFO V1 \_       | Dimensioni della struttura [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) nella versione 4,0.             |
| \_Dimensioni LVITEM V1 \_              | Dimensioni della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) nella versione 4,0.                           |
| \_Dimensioni LVITEM V5 \_              | Dimensioni della struttura [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) nella versione 6,0.                           |
| \_Dimensioni LVTILEINFO V5 \_          | Dimensioni della struttura [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) nella versione 6,0.                   |
| \_Dimensioni MCHITTESTINFO V1 \_       | Dimensioni della struttura [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) nella versione 4,0.             |
| \_Dimensioni NMLVCUSTOMDRAW V3 \_      | Dimensioni della struttura [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) nella versione 4,7.           |
| \_Dimensioni NMTTDISPINFO V1 \_        | Dimensioni della struttura [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) nella versione 4,0.               |
| \_Dimensioni NMTVCUSTOMDRAW V3 \_      | Dimensioni della struttura [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) nella versione 4,7.           |
| \_Dimensioni PROPSHEETHEADER V1 \_     | Dimensioni della struttura [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) nella versione 4,0.         |
| \_Dimensioni PROPSHEETPAGE V1 \_       | Dimensioni della struttura [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) nella versione 4,0.             |
| \_Dimensioni REBARBANDINFO V3 \_       | Dimensioni della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) nella versione 4,7.             |
| \_Dimensioni REBARBANDINFO V6 \_       | Dimensioni della struttura [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) nella versione 6,0.             |
| \_Dimensioni TTTOOLINFO V1 \_          | Dimensioni della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) nella versione 4,0.                       |
| \_Dimensioni TTTOOLINFO v2 \_          | Dimensioni della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) nella versione 4,7.                       |
| \_Dimensioni TTTOOLINFO V3 \_          | Dimensioni della struttura [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) nella versione 6,0.                       |
| \_Dimensioni TVINSERTSTRUCT V1 \_      | Dimensioni della struttura [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) nella versione 4,0.           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a>Utilizzo di DllGetVersion per determinare il numero di versione

La funzione [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) può essere chiamata da un'applicazione per determinare quale versione della dll è presente nel sistema.

[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) restituisce una struttura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . Oltre alle informazioni fornite tramite [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** fornisce anche il numero di hotfix che identifica il Service Pack installato più recente, che fornisce un modo più efficace per confrontare i numeri di versione. Poiché il primo membro di **DLLVERSIONINFO2** è una struttura **DLLVERSIONINFO** , la struttura successiva è compatibile con le versioni precedenti.


La funzione di esempio seguente `GetVersion` carica una DLL specificata e tenta di chiamare la relativa funzione [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) . Se ha esito positivo, usa una macro per comprimere i numeri di versione principale e secondaria dalla struttura [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) in un **valore DWORD** restituito all'applicazione chiamante. Se la DLL non esporta **DllGetVersion**, la funzione restituisce zero. È possibile modificare la funzione per gestire la possibilità che **DllGetVersion** restituisca una struttura [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) . In tal caso, usare le informazioni contenute nel membro **ullVersion** della struttura **DLLVERSIONINFO2** per confrontare le versioni, i numeri di build e le versioni Service Pack. La macro [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) semplifica l'attività di confronto di questi valori con quelli in **ullVersion**.

> [!Note]  
> L'uso errato di [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) può causare rischi per la sicurezza. Per informazioni su come caricare correttamente le dll con versioni diverse di Windows, vedere la documentazione di **LoadLibrary** .

 


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

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

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



Nell'esempio di codice seguente viene illustrato come utilizzare `GetVersion` per verificare se ComCtl32.dll è la versione 6,0 o successiva.


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a>Versioni del progetto

Per assicurarsi che l'applicazione sia compatibile con diverse versioni di destinazione di un file con estensione dll, le macro della versione sono presenti nei file di intestazione. Queste macro vengono utilizzate per definire, escludere o ridefinire determinate definizioni per versioni diverse della DLL. Per una descrizione approfondita di queste macro, vedere [uso delle intestazioni di Windows](/windows/desktop/WinProg/using-the-windows-headers) .

Ad esempio, il nome di macro **\_ Win32 \_ IE** si trova in genere nelle intestazioni precedenti. L'utente è responsabile della definizione della macro come numero esadecimale. Questo numero di versione definisce la versione di destinazione dell'applicazione che usa la DLL. La tabella seguente illustra i numeri di versione disponibili e l'effetto di ogni utente sull'applicazione.



| Versione | Descrizione                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x0300  | L'applicazione è compatibile con ComCtl32.dll versione 4,70 e successive. L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,70. |
| 0x0400  | L'applicazione è compatibile con ComCtl32.dll versione 4,71 e successive. L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,71. |
| 0x0401  | L'applicazione è compatibile con ComCtl32.dll versione 4,72 e successive. L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 4,72. |
| 0x0500  | L'applicazione è compatibile con ComCtl32.dll versione 5,80 e successive. L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 5,80. |
| 0x0501  | L'applicazione è compatibile con ComCtl32.dll versione 5,81 e successive. L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 5,81. |
| 0x0600  | L'applicazione è compatibile con ComCtl32.dll versione 6,0 e successive. L'applicazione non è in grado di implementare le funzionalità aggiunte dopo la versione 6,0.   |



 

Se non si definisce la macro di **\_ \_ IE Win32** nel progetto, questa viene definita automaticamente come 0x0500. Per definire un valore diverso, è possibile aggiungere quanto segue alle direttive del compilatore nel file make; sostituire il numero di versione desiderato per 0x0400.


```C++
/D _WIN32_IE=0x0400
```



Un altro metodo consiste nell'aggiungere una riga simile alla seguente nel codice sorgente prima di includere i file di intestazione della shell. Sostituire il numero di versione desiderato per 0x0400.


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sui controlli comuni](common-controls-intro.md)
</dt> </dl>

 

 