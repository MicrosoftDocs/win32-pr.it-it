---
title: Uso delle intestazioni Windows
description: Usare i Windows di intestazione per creare applicazioni che usano l'API Windows.
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- Windows API, file di intestazione
- C2065
- Winver
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 886c5601683cc03fb2486f8be3b69f31c4619b721276babbc2c3e31e28c0a022
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119643591"
---
# <a name="using-the-windows-headers"></a>Uso delle intestazioni Windows

I file di intestazione per l Windows API consentono di creare applicazioni a 32 e a 64 bit. Includono dichiarazioni per le versioni Unicode e ANSI dell'API. Per altre informazioni, vedere [Unicode nell'API Windows](/windows/desktop/Intl/unicode-in-the-windows-api). Usano tipi [di dati che](windows-data-types.md) consentono di compilare versioni a 32 e a 64 bit dell'applicazione da una singola codebase del codice sorgente. Per altre informazioni, vedere [Getting Ready for 64-bit Windows](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows). Tra le funzionalità aggiuntive sono [incluse le annotazioni di intestazione](header-annotations.md) e il controllo dei tipi [STRICT.](strict-type-checking.md)

-   [Visual C++ e i Windows di intestazione](#visual-c-and-the-windows-header-files)
-   [Macro per dichiarazioni condizionali](#macros-for-conditional-declarations)
-   [Impostazione di WINVER \_ o WIN32 \_ WINNT](#setting-winver-or-_win32_winnt)
-   [Controllo della creazione di un pacchetto di strutture](#controlling-structure-packing)
-   [Compilazioni più veloci con file di intestazione più piccoli](#faster-builds-with-smaller-header-files)
-   [Argomenti correlati](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ e i Windows di intestazione

Microsoft Visual C++ include copie dei file Windows di intestazione corrente al momento Visual C++ è stato rilasciato. Pertanto, se si installano file di intestazione aggiornati da un SDK, è possibile che nel computer Windows più versioni dei file di intestazione dei file di intestazione. Se non si è certi di usare la versione più recente dei file di intestazione dell'SDK, si riceverà il codice di errore seguente durante la compilazione di codice che usa funzionalità introdotte dopo il rilascio di Visual C++: errore C2065: identificatore non dichiarato.

## <a name="macros-for-conditional-declarations"></a>Macro per dichiarazioni condizionali

Alcune funzioni che dipendono da una determinata versione di Windows vengono dichiarate tramite codice condizionale. In questo modo è possibile usare il compilatore per rilevare se l'applicazione usa funzioni non supportate nelle relative versioni di destinazione di Windows. Per compilare un'applicazione che usa queste funzioni, è necessario definire le macro appropriate. In caso contrario, verrà visualizzato il messaggio di errore C2065.

I Windows di intestazione usano macro per indicare quali versioni di Windows supportano molti elementi di programmazione. Pertanto, è necessario definire queste macro per usare le nuove funzionalità introdotte in ogni versione principale del sistema operativo. I singoli file di intestazione possono usare macro diverse. Pertanto, se si verificano problemi di compilazione, controllare il file di intestazione che contiene la definizione per le definizioni condizionali. Per altre informazioni, vedere SdkDdkVer.h.

Nella tabella seguente vengono descritte le macro preferite usate nei file Windows di intestazione. Se si definisce NTDDI \_ VERSION, è necessario definire anche \_ WIN32 \_ WINNT.



| Sistema minimo richiesto                       | Valore per NTDDI \_ VERSION            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 "19H1"                        | **NTDDI \_ WIN10 \_ 19H1** (0x0A000007) |
| Windows 10 1809 "Redstone 5"                  | **NTDDI \_ WIN10 \_ RS5** (0x0A000006)  |
| Windows 10 1803 "Redstone 4"                  | **NTDDI \_ WIN10 \_ RS4** (0x0A000005)  |
| Windows 10 1709 "Redstone 3"                  | **NTDDI \_ WIN10 \_ RS3** (0x0A000004)  |
| Windows 10 1703 "Redstone 2"                  | **NTDDI \_ WIN10 \_ RS2** (0x0A000003)  |
| Windows 10 1607 "Redstone 1"                  | **NTDDI \_ WIN10 \_ RS1** (0x0A000002)  |
| Windows 10 1511 "Soglia 2"                 | **NTDDI \_ WIN10 \_ TH2** (0x0A000001)  |
| Windows 10 1507 "Soglia"                   | **NTDDI \_ WIN10** (0x0A000000)       |
| Windows 8.1                                   | **NTDDI \_ WINBLUE** (0x06030000)     |
| Windows 8                                     | **NTDDI \_ WIN8** (0x06020000)        |
| Windows 7                                     | **NTDDI \_ WIN7** (0x06010000)        |
| Windows Server 2008                           | **NTDDI \_ WS08** (0x06000100)        |
| Windows Vista con Service Pack 1 (SP1)       | **NTDDI \_ VISTASP1** (0x06000100)    |
| Windows Vista                                 | **NTDDI \_ VISTA** (0x06000000)       |
| Windows Server 2003 con Service Pack 2 (SP2) | **NTDDI \_ WS03SP2** (0x05020200)     |
| Windows Server 2003 con Service Pack 1 (SP1) | **NTDDI \_ WS03SP1** (0x05020100)     |
| Windows Server 2003                           | **NTDDI \_ WS03** (0x05020000)        |
| Windows XP con Service Pack 3 (SP3)          | **NTDDI \_ WINXPSP3** (0x05010300)    |
| Windows XP con Service Pack 2 (SP2)          | **NTDDI \_ WINXPSP2** (0x05010200)    |
| Windows XP con Service Pack 1 (SP1)          | **NTDDI \_ WINXPSP1** (0x05010100)    |
| Windows XP                                    | **NTDDI \_ WINXP** (0x05010000)       |



 

Nelle tabelle seguenti vengono descritte le altre macro usate nei file Windows di intestazione.



| Sistema minimo richiesto                           | Valore minimo per \_ WIN32 \_ WINNT e WINVER |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ WIN32 \_ WINNT \_ WIN10** (0x0A00)          |
| Windows 8.1                                       | **\_ WIN32 \_ WINNT \_ WINBLUE** (0x0603)        |
| Windows 8                                         | **\_ WIN32 \_ WINNT \_ WIN8** (0x0602)           |
| Windows 7                                         | **\_ WIN32 \_ WINNT \_ WIN7** (0x0601)           |
| Windows Server 2008                               | **\_ WIN32 \_ WINNT \_ WS08** (0x0600)           |
| Windows Vista                                     | **\_ WIN32 \_ WINNT \_ VISTA** (0x0600)          |
| Windows Server 2003 con SP1, Windows XP con SP2 | **\_ WIN32 \_ WINNT \_ WS03** (0x0502)           |
| Windows Server 2003, Windows XP                   | **\_ WIN32 \_ WINNT \_ WINXP** (0x0501)          |



 



| Versione minima richiesta          | Valore minimo di \_ Win32 \_ IE      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11.0            | **\_ WIN32 \_ IE \_ IE110** (0x0A00)   |
| Internet Explorer 10.0            | **\_ WIN32 \_ IE \_ IE100** (0x0A00)   |
| Internet Explorer 9.0             | **\_ WIN32 \_ IE \_ IE90** (0x0900)    |
| Internet Explorer 8.0             | **\_ WIN32 \_ IE \_ IE80** (0x0800)    |
| Internet Explorer 7.0             | **\_ WIN32 \_ IE \_ IE70** (0x0700)    |
| Internet Explorer 6.0 SP2         | **\_ WIN32 \_ \_ IE60SP2** (0x0603) |
| Internet Explorer 6.0 SP1         | **\_ WIN32 \_ \_ IE60SP1** (0x0601) |
| Internet Explorer 6.0             | **\_ WIN32 \_ IE \_ IE60** (0x0600)    |
| Internet Explorer 5.5             | **\_ WIN32 \_ IE \_ IE55** (0x0550)    |
| Internet Explorer 5.01            | **\_ WIN32 \_ IE \_ IE501** (0x0501)   |
| Internet Explorer 5.0, 5.0a, 5.0b | **\_ WIN32 \_ IE \_ IE50** (0x0500)    |



 

## <a name="setting-winver-or-_win32_winnt"></a>Impostazione di WINVER \_ o WIN32 \_ WINNT

È possibile definire questi simboli usando l'istruzione define in ogni file di origine o specificando l'opzione del compilatore \# /D supportata da Visual C++.

Ad esempio, per impostare WINVER nel file di origine, usare l'istruzione seguente:

`#define WINVER 0x0502`

Per impostare \_ WIN32 \_ WINNT nel file di origine, usare l'istruzione seguente:

`#define _WIN32_WINNT 0x0502`

Per impostare \_ WIN32 \_ WINNT usando l'opzione del compilatore /D, usare il comando seguente:

**cl -c /D \_ WIN32 \_ WINNT=0x0502** **.cpp** _di_ origine

Per informazioni sull'uso dell'opzione del compilatore /D, vedere [/D (definizioni del preprocessore).](/cpp/build/reference/d-preprocessor-definitions)

Si noti che alcune funzionalità introdotte nella versione più recente di Windows possono essere aggiunte a un Service Pack per una versione precedente di Windows. Pertanto, per specificare come destinazione un Service Pack, potrebbe essere necessario definire WIN32 WINNT con il valore per la \_ versione successiva del sistema operativo \_ principale. Ad esempio, la [**funzione GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) è stata introdotta in Windows Server 2003 ed è definita in modo condizionale se \_ WIN32 WINNT è \_ 0x0502 o versione successiva. Questa funzione è stata aggiunta anche a Windows XP con SP1. Pertanto, se si definisce WIN32 WINNT come 0x0501 come destinazione di Windows XP, si perderanno le funzionalità definite in Windows XP con \_ \_ SP1.

## <a name="controlling-structure-packing"></a>Controllo della creazione di un pacchetto di strutture

I progetti devono essere compilati in modo da usare la struttura predefinita, che attualmente è di 8 byte perché il tipo integrale più grande è 8 byte. In questo modo si garantisce che tutti i tipi di struttura all'interno dei file di intestazione siano compilati nell'applicazione con lo stesso allineamento previsto Windows'API. Garantisce inoltre che le strutture con valori a 8 byte siano allineate correttamente e non causeranno errori di allineamento nei processori che applicano l'allineamento dei dati.

Per altre informazioni, vedere [/Zp (allineamento dei membri struct) o](/cpp/build/reference/zp-struct-member-alignment) [pack.](/cpp/preprocessor/pack)

## <a name="faster-builds-with-smaller-header-files"></a>Compilazioni più veloci con file di intestazione più piccoli

È possibile ridurre le dimensioni dei file Windows di intestazione escludendo alcune delle dichiarazioni API meno comuni, come indicato di seguito:

-   Definire WIN32 LEAN E MEAN per escludere API come \_ \_ \_ Cryptography, DDE, RPC, Shell e Windows Socket.

    `#define WIN32_LEAN_AND_MEAN`

-   Definire uno o più simboli *dell'API* NO per escludere l'API. Ad esempio, NOCOMM esclude l'API di comunicazione seriale. Per un elenco dei simboli DI *API* NO supportati, vedere Windows.h.

    `#define NOCOMM`

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Windows Sito di download dell'SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 