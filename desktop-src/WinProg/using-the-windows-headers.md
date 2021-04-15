---
title: Uso delle intestazioni di Windows
description: Usare i file di intestazione di Windows per creare applicazioni che usano l'API Windows.
ms.assetid: a4def563-8ddc-4630-ae8a-86c07cf98374
keywords:
- API Windows, file di intestazione
- C2065
- WINVER
- _WIN32_WINDOWS
- _WIN32_WINNT
- _WIN32_IE
- WIN32_LEAN_AND_MEAN
ms.topic: article
ms.date: 01/22/2020
ms.openlocfilehash: 4d27b14a6e545db9a9a38c205012b149942adf7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399526"
---
# <a name="using-the-windows-headers"></a>Uso delle intestazioni di Windows

I file di intestazione per l'API Windows consentono di creare applicazioni a 32 e 64 bit. Sono incluse le dichiarazioni per le versioni Unicode e ANSI dell'API. Per ulteriori informazioni, vedere [Unicode nell'API Windows](/windows/desktop/Intl/unicode-in-the-windows-api). Usano [tipi di dati](windows-data-types.md) che consentono di compilare entrambe le versioni a 32 e 64 bit dell'applicazione da un'unica base di codice sorgente. Per altre informazioni, vedere [preparazione per Windows a 64 bit](/windows/desktop/WinProg64/getting-ready-for-64-bit-windows). Le funzionalità aggiuntive includono le [annotazioni di intestazione](header-annotations.md) e [il controllo dei tipi rigoroso](strict-type-checking.md).

-   [Visual C++ e i file di intestazione di Windows](#visual-c-and-the-windows-header-files)
-   [Macro per le dichiarazioni condizionali](#macros-for-conditional-declarations)
-   [Impostazione di WINVER o \_ Win32 \_ WinNT](#setting-winver-or-_win32_winnt)
-   [Controllo della compressione della struttura](#controlling-structure-packing)
-   [Compilazioni più veloci con file di intestazione più piccoli](#faster-builds-with-smaller-header-files)
-   [Argomenti correlati](#related-topics)

## <a name="visual-c-and-the-windows-header-files"></a>Visual C++ e i file di intestazione di Windows

Microsoft Visual C++ include le copie dei file di intestazione di Windows correnti al momento del rilascio Visual C++. Se pertanto si installano i file di intestazione aggiornati da un SDK, è possibile che si verifichino più versioni dei file di intestazione di Windows nel computer. Se non si è certi di usare la versione più recente dei file di intestazione SDK, verrà visualizzato il codice di errore seguente durante la compilazione del codice che usa le funzionalità introdotte dopo il rilascio di Visual C++: errore C2065: identificatore non dichiarato.

## <a name="macros-for-conditional-declarations"></a>Macro per le dichiarazioni condizionali

Alcune funzioni che dipendono da una particolare versione di Windows vengono dichiarate usando il codice condizionale. In questo modo è possibile utilizzare il compilatore per rilevare se l'applicazione utilizza funzioni non supportate nelle relative versioni di destinazione di Windows. Per compilare un'applicazione che usa queste funzioni, è necessario definire le macro appropriate. In caso contrario, verrà visualizzato il messaggio di errore C2065.

I file di intestazione di Windows utilizzano le macro per indicare quali versioni di Windows supportano molti elementi di programmazione. Pertanto, è necessario definire queste macro per utilizzare le nuove funzionalità introdotte in ogni versione principale del sistema operativo. I singoli file di intestazione possono utilizzare macro diverse; pertanto, se si verificano problemi di compilazione, controllare il file di intestazione contenente la definizione per le definizioni condizionali. Per ulteriori informazioni, vedere SdkDdkVer. h.

Nella tabella seguente vengono descritte le macro preferite utilizzate nei file di intestazione di Windows. Se si definisce la \_ versione di NTDDI, è necessario definire anche il \_ \_ WinNT Win32.



| Requisito minimo di sistema                       | Valore per la \_ versione di NTDDI            |
|-----------------------------------------------|-------------------------------------|
| Windows 10 1903 "19H1"                        | **NTDDI \_ WIN10 \_ 19H1** (0x0A000007) |
| Windows 10 1809 "Redstone 5"                  | **NTDDI \_ WIN10 \_ RS5** (0x0A000006)  |
| Windows 10 1803 "Redstone 4"                  | **NTDDI \_ WIN10 \_ RS4** (0x0A000005)  |
| Windows 10 1709 "Redstone 3"                  | **NTDDI \_ WIN10 \_ RS3** (0x0A000004)  |
| Windows 10 1703 "Redstone 2"                  | **NTDDI \_ WIN10 \_ RS2** (0x0A000003)  |
| Windows 10 1607 "Redstone 1"                  | **NTDDI \_ WIN10 \_ RS1** (0x0A000002)  |
| Windows 10 1511 "soglia 2"                 | **NTDDI \_ WIN10 \_ Th2** (0x0A000001)  |
| Windows 10 1507 "soglia"                   | **NTDDI \_ WIN10** (0x0A000000)       |
| Windows 8.1                                   | **NTDDI \_ WINBLUE** (0x06030000)     |
| Windows 8                                     | **NTDDI \_ WIN8** (0x06020000)        |
| Windows 7                                     | **NTDDI \_ WIN7** (0x06010000)        |
| Windows Server 2008                           | **NTDDI \_ WS08** (0x06000100)        |
| Windows Vista con Service Pack 1 (SP1)       | **NTDDI \_ VISTASP1** (0x06000100)    |
| Windows Vista                                 | **NTDDI \_ VISTA** (0x06000000)       |
| Windows Server 2003 con Service Pack 2 (SP2) | **NTDDI \_ WS03SP2** (0x05020200)     |
| Windows Server 2003 con Service Pack 1 (SP1) | **NTDDI \_ WS03SP1** (0x05020100)     |
| Windows Server 2003                           | **NTDDI \_ WS03** (0x05020000)        |
| Windows XP con Service Pack 3 (SP3)          | **NTDDI \_ WINXPSP3** (0x05010300)    |
| Windows XP con Service Pack 2 (SP2)          | **NTDDI \_ WINXPSP2** (0x05010200)    |
| Windows XP con Service Pack 1 (SP1)          | **NTDDI \_ WINXPSP1** (0x05010100)    |
| Windows XP                                    | **NTDDI \_ WINXP** (0x05010000)       |



 

Nelle tabelle seguenti vengono descritte le altre macro utilizzate nei file di intestazione di Windows.



| Requisito minimo di sistema                           | Valore minimo per \_ Win32 \_ WinNT e winver |
|---------------------------------------------------|---------------------------------------------|
| Windows 10                                        | **\_ Win32 \_ WinNT \_ WIN10** (0x0A00)          |
| Windows 8.1                                       | **\_ Win32 \_ WinNT \_ WINBLUE** (0x0603)        |
| Windows 8                                         | **\_ Win32 \_ WinNT \_ Win8** (0x0602)           |
| Windows 7                                         | **\_ \_ Winnt winnt \_ Win32** (0x0601)           |
| Windows Server 2008                               | **\_ Win32 \_ WinNT \_ WS08** (0x0600)           |
| Windows Vista                                     | **\_ Win32 \_ WinNT \_ vista** (0x0600)          |
| Windows Server 2003 con SP1, Windows XP con SP2 | **\_ Win32 \_ WinNT \_ WS03** (0x0502)           |
| Windows Server 2003, Windows XP                   | **\_ Win32 \_ WinNT \_ WinXP** (0x0501)          |



 



| Versione minima richiesta          | Valore minimo di \_ \_ IE Win32      |
|-----------------------------------|-----------------------------------|
| Internet Explorer 11,0            | **\_ Win32 \_ IE \_ IE110** (0x0A00)   |
| Internet Explorer 10,0            | **\_ Win32 \_ IE \_ IE100** (0x0A00)   |
| Internet Explorer 9.0             | **\_ Win32 \_ IE \_ IE90** (0x0900)    |
| Internet Explorer 8.0             | **\_ Win32 \_ IE \_ IE80** (0x0800)    |
| Internet Explorer 7.0             | **\_ Win32 \_ IE \_ IE70** (0x0700)    |
| Internet Explorer 6,0 SP2         | **\_ Win32 \_ IE \_ IE60SP2** (0x0603) |
| Internet Explorer 6,0 SP1         | **\_ Win32 \_ IE \_ IE60SP1** (0x0601) |
| Internet Explorer 6.0             | **\_ Win32 \_ IE \_ IE60** (0x0600)    |
| Internet Explorer 5.5             | **\_ Win32 \_ IE \_ Ie55** (0x0550)    |
| Internet Explorer 5,01            | **\_ Win32 \_ IE \_ IE501** (0x0501)   |
| Internet Explorer 5,0, 5.0 a, 5.0 b | **\_ Win32 \_ IE \_ IE50** (0x0500)    |



 

## <a name="setting-winver-or-_win32_winnt"></a>Impostazione di WINVER o \_ Win32 \_ WinNT

È possibile definire questi simboli usando l' \# istruzione define in ogni file di origine oppure specificando l'opzione del compilatore/d supportata da Visual C++.

Per impostare WINVER nel file di origine, ad esempio, usare l'istruzione seguente:

`#define WINVER 0x0502`

Per impostare \_ Win32 \_ WinNT nel file di origine, utilizzare l'istruzione seguente:

`#define _WIN32_WINNT 0x0502`

Per impostare \_ Win32 \_ WinNT utilizzando l'opzione del compilatore/d, utilizzare il comando seguente:

**cl-c/d \_ WIN32 \_ WinNT = 0x0502** _source_**. cpp**

Per informazioni sull'uso dell'opzione del compilatore/D, vedere [/d (definizioni preprocessore)](/cpp/build/reference/d-preprocessor-definitions).

Si noti che alcune funzionalità introdotte nella versione più recente di Windows possono essere aggiunte a un Service Pack per una versione precedente di Windows. Pertanto, per fare riferimento a un Service Pack, potrebbe essere necessario definire \_ Win32 \_ WinNT con il valore per la prossima versione principale del sistema operativo. Ad esempio, la funzione [**GetDllDirectory**](/windows/desktop/api/winbase/nf-winbase-getdlldirectorya) è stata introdotta in Windows Server 2003 e viene definita in modo condizionale se \_ Win32 \_ WinNT è 0x0502 o versione successiva. Questa funzione è stata aggiunta anche a Windows XP con SP1. Pertanto, se si desidera definire \_ Win32 \_ WinNT come 0X0501 per Windows XP, è possibile che si perdano le funzionalità definite in Windows XP con SP1.

## <a name="controlling-structure-packing"></a>Controllo della compressione della struttura

I progetti devono essere compilati in modo da usare il pacchetto di struttura predefinito, che è attualmente di 8 byte perché il tipo integrale più grande è 8 byte. In questo modo si garantisce che tutti i tipi di struttura all'interno dei file di intestazione vengano compilati nell'applicazione con lo stesso allineamento previsto dall'API Windows. Garantisce inoltre che le strutture con valori a 8 byte siano allineate correttamente e non provochino errori di allineamento nei processori che applicano l'allineamento dei dati.

Per altre informazioni, vedere [/ZP (allineamento membri struct)](/cpp/build/reference/zp-struct-member-alignment) o [Pack](/cpp/preprocessor/pack).

## <a name="faster-builds-with-smaller-header-files"></a>Compilazioni più veloci con file di intestazione più piccoli

È possibile ridurre le dimensioni dei file di intestazione di Windows escludendo alcune delle dichiarazioni API meno comuni, come indicato di seguito:

-   Definire \_ Lean \_ e Mean Win32 \_ per escludere le API, ad esempio crittografia, DDE, RPC, Shell e Windows Sockets.

    `#define WIN32_LEAN_AND_MEAN`

-   Definire uno o più simboli nessuna *API* per escludere l'API. Ad esempio, NOCOMM esclude l'API di comunicazione seriale. Per un elenco di simboli di supporto senza *API* , vedere Windows. h.

    `#define NOCOMM`

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Sito di download Windows SDK](https://msdn.microsoft.com/windowsserver/bb980924.aspx)
</dt> </dl>

 

 