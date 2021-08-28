---
title: Tipi di dati di Windows (BaseTsd.h)
description: I tipi di dati supportati da Windows vengono usati per definire i valori restituiti dalla funzione, i parametri di funzione e messaggio e i membri della struttura.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- tipi di dati
- tipi di dati, Windows
- API Windows
- Windows API, tipi di dati
- APIENTRY
- ATOM
- BOOL
- BOOLEAN
- BYTE
- CALLBACK
- CCHAR
- CHAR
- COLORREF
- CONST
- DWORD
- DWORDLONG
- DWORD_PTR
- DWORD32
- DWORD64
- FLOAT
- HACCEL
- HALF_PTR
- HANDLE
- HBITMAP
- HBRUSH
- HCOLORSPACE
- HCONV
- HCONVLIST
- HCURSOR
- HDC
- HDDEDATA
- HDESK
- HDROP
- HDWP
- HENHMETAFILE
- HFILE
- HFONT
- HGDIOBJ
- HGLOBAL
- HHOOK
- HICON
- HINSTANCE
- HKEY
- HKL
- HLOCAL
- HMENU
- HMETAFILE
- HMODULE
- HMONITOR
- HPALETTE
- HPEN
- HRESULT
- HRGN
- HRSRC
- HSZ
- HWINSTA
- HWND
- INT
- INT_PTR
- INT8
- INT16
- INT32
- INT64
- LANGID
- LCID
- LCTYPE
- LGRPID
- LONG
- LONGLONG
- LONG_PTR
- LONG32
- LONG64
- LPARAM
- LPBOOL
- LPBYTE
- LPCOLORREF
- LPCSTR
- LPCTSTR
- LPCVOID
- LPCWSTR
- LPDWORD
- LPHANDLE
- LPINT
- LPLONG
- LPSTR
- LPTSTR
- LPVOID
- LPWORD
- LPWSTR
- LRESULT
- PBOOL
- PBOOLEAN
- PBYTE
- PCHAR
- PCSTR
- PCTSTR
- PCWSTR
- PDWORD
- PDWORDLONG
- PDWORD_PTR
- PDWORD32
- PDWORD64
- PFLOAT
- PHALF_PTR
- PHANDLE
- PHKEY
- PINTA
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- PLCID
- PLONG
- PLONGLONGLONG
- PLONG_PTR
- PLONG32
- PLONG64
- POINTER_32
- POINTER_64
- POINTER_SIGNED
- POINTER_UNSIGNED
- PSHORT
- PSIZE_T
- PSSIZE_T
- PSTR
- PTBYTE
- PTCHAR
- PTSTR
- PUCHAR
- PUHALF_PTR
- PUINT
- PUINT_PTR
- PUINT8
- PUINT16
- PUINT32
- PUINT64
- PULONG
- PULONGLONG
- PULONG_PTR
- PULONG32
- PULONG64
- PUSHORT
- PVOID
- PWCHAR
- PWORD
- PWSTR
- QWORD
- SC_HANDLE
- SC_LOCK
- SERVICE_STATUS_HANDLE
- SHORT
- SIZE_T
- SSIZE_T
- TBYTE
- TCHAR
- UCHAR
- UHALF_PTR
- UINT
- UINT_PTR
- UINT8
- UINT16
- UINT32
- UINT64
- ULONG
- ULONGLONG
- ULONG_PTR
- ULONG32
- ULONG64
- UNICODE_STRING
- USHORT
- USN
- VUOTO
- WCHAR
- WINAPI
- WORD
- WPARAM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3002912cafbdf2dd4fe62c19fe3faef302da8c9b
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2021
ms.locfileid: "122626337"
---
# <a name="windows-data-types"></a>Tipi di dati di Windows

I tipi di dati supportati da Windows vengono usati per definire i valori restituiti dalla funzione, i parametri di funzione e messaggio e i membri della struttura. Definiscono le dimensioni e il significato di questi elementi. Per altre informazioni sui tipi di dati C/C++ sottostanti, vedere [Intervalli di tipi di dati](/cpp/cpp/data-type-ranges?view=vs-2019).

La tabella seguente contiene i tipi seguenti: carattere, integer, booleano, puntatore e handle. I tipi carattere, integer e booleano sono comuni alla maggior parte dei compilatori C. La maggior parte dei nomi di tipo puntatore inizia con un prefisso P o LP. Gli handle fanno riferimento a una risorsa caricata in memoria.

Per altre informazioni sulla gestione di interi a 64 bit, vedere [Numeri interi grandi](large-integers.md).



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Tipo di dati</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></td>
<td>Convenzione di chiamata per le funzioni di sistema.<br/> Questo tipo viene dichiarato in WinDef.h come indicato di seguito:<br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></td>
<td>Atom. Per altre informazioni, vedere <a href="/windows/desktop/dataxchg/about-atom-tables">Informazioni sulle tabelle Atom</a>.<br/> Questo tipo viene dichiarato in WinDef.h come indicato di seguito:<br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></td>
<td>Variabile booleana (deve essere <strong>TRUE</strong> o <strong>FALSE).</strong><br/> Questo tipo viene dichiarato in WinDef.h come indicato di seguito:<br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></td>
<td>Variabile booleana (deve essere <strong>TRUE</strong> o <strong>FALSE).</strong><br/> Questo tipo viene dichiarato in WinNT.h come indicato di seguito:<br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></td>
<td>Byte (8 bit).<br/> Questo tipo viene dichiarato in WinDef.h come segue:<br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></td>
<td>Convenzione di chiamata per le funzioni di callback.<br/> Questo tipo viene dichiarato in WinDef.h come segue:<br/> <code>#define CALLBACK __stdcall</code><br/> <strong>CALLBACK,</strong> <strong>WINAPI</strong>e <strong>APIENTRY</strong> vengono tutti usati per definire le funzioni con la __stdcall di chiamata. La maggior parte delle funzioni nell Windows API viene dichiarata usando <strong>WINAPI.</strong> È possibile usare <strong>CALLBACK per le</strong> funzioni di callback implementate per identificare la funzione come funzione di callback.<br/></td>
</tr>
<tr class="odd">
<td><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></td>
<td>Carattere ANSI (Windows a 8 bit).<br/> Questo tipo viene dichiarato in WinNT.h come indicato di seguito:<br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></td>
<td>Carattere ANSI (Windows a 8 bit). Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere.</a><br/> Questo tipo viene dichiarato in WinNT.h come indicato di seguito:<br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></td>
<td>Valore del colore rosso, verde, blu (RGB) (32 bit). Per informazioni su questo tipo, vedere <a href="/windows/desktop/gdi/colorref"><strong>COLORREF.</strong></a><br/> Questo tipo viene dichiarato in WinDef.h come segue:<br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span id="CONST"></span><span id="const"></span><strong>CONST</strong></td>
<td>Variabile il cui valore deve rimanere costante durante l'esecuzione. <br/> Questo tipo viene dichiarato in WinDef.h come segue:<br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></td>
<td>Intero senza segno a 32 bit. L'intervallo è compreso tra 0 e 4294967295 decimale.<br/> Questo tipo viene dichiarato in IntSafe.h come indicato di seguito:<br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></td>
<td>Intero senza segno a 64 bit. L'intervallo è compreso tra 0 e 18446744073709551615 decimale.<br/> Questo tipo viene dichiarato in IntSafe.h come indicato di seguito:<br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></td>
<td>Tipo long senza segno per la precisione del puntatore. Usare quando si esegue il cast di un puntatore a un tipo long per eseguire l'aritmetica dei puntatori. Usato comunemente anche per i parametri generali a 32 bit che sono stati estesi a 64 bit in Windows.<br/> Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:<br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></td>
<td>Intero senza segno a 32 bit.<br/> Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:<br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></td>
<td>Intero senza segno a 64 bit.<br/> Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:<br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span id="FLOAT"></span><span id="float"></span><strong>GALLEGGIANTE</strong></td>
<td>Variabile a virgola mobile.<br/> Questo tipo viene dichiarato in WinDef.h come segue:<br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></td>
<td>Handle per una tabella <a href="/windows/desktop/menurc/keyboard-accelerators">dei tasti di scelta rapida.</a><br/> Questo tipo viene dichiarato in WinDef.h come segue:<br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></td>
<td>Metà delle dimensioni di un puntatore. Usare all'interno di una struttura che contiene un puntatore e due campi piccoli.<br/> Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:<br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef int HALF_PTR;
#else
 typedef short HALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="odd">
<td><span id="HANDLE"></span><span id="handle"></span><strong>GESTIRE</strong></td>
<td><p>Handle per un oggetto .</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></td>
<td><p>Handle per una <a href="/windows/desktop/gdi/bitmaps">bitmap.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></td>
<td><p>Handle per un <a href="/windows/desktop/gdi/brushes">pennello.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></td>
<td><p>Handle per uno <a href="/previous-versions//dd316799(v=vs.85)">spazio dei colori.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></td>
<td><p>Handle per una conversazione DDE (Dynamic Data Exchange).</p>
<p>Questo tipo viene dichiarato in Ddeml.h come segue:</p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></td>
<td><p>Handle per un elenco di conversazioni DDE.</p>
<p>Questo tipo viene dichiarato in Ddeml.h come segue:</p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></td>
<td><p>Handle per un <a href="/windows/desktop/menurc/cursors">cursore.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></td>
<td><p>Handle per un <a href="/windows/desktop/gdi/device-context-types">contesto di dispositivo.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></td>
<td><p>Handle per i dati DDE.</p>
<p>Questo tipo viene dichiarato in Ddeml.h come segue:</p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></td>
<td><p>Handle per un <a href="/windows/desktop/winstation/desktops">oggetto desktop.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></td>
<td><p>Handle per una struttura di rilascio interna.</p>
<p>Questo tipo viene dichiarato in ShellApi.h come indicato di seguito:</p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></td>
<td><p>Handle per una struttura di posizione della finestra posticipata.</p>
<p>Questo tipo viene dichiarato in WinUser.h come indicato di seguito:</p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></td>
<td><p>Handle per un <a href="/windows/desktop/gdi/metafiles">metafile avanzato.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></td>
<td><p>Handle per un file aperto da <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>e non <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>da CreateFile.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></td>
<td><p>Handle per un tipo <a href="/windows/desktop/gdi/about-fonts">di carattere</a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></td>
<td><p>Handle per un oggetto GDI.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></td>
<td><p>Handle per un blocco di memoria globale.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></td>
<td><p>Handle per un <a href="/windows/desktop/winmsg/hooks">hook.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></td>
<td><p>Handle per <a href="/windows/desktop/menurc/icons">un'icona</a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></td>
<td><p>Handle per un'istanza di . Si tratta dell'indirizzo di base del modulo in memoria.</p>
<p><strong>HMODULE</strong> e <strong>HINSTANCE sono</strong> gli stessi oggi, ma rappresentavano elementi diversi in un Windows a 16 bit.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></td>
<td><p>Handle per una chiave del Registro di sistema.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></td>
<td><p>Identificatore delle impostazioni locali di input.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></td>
<td><p>Handle per un blocco di memoria locale.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></td>
<td><p>Handle per un <a href="/windows/desktop/menurc/menus">menu</a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></td>
<td><p>Handle per un <a href="/windows/desktop/gdi/metafiles">metafile.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></td>
<td><p>Handle per un modulo. è l'indirizzo di base del modulo in memoria.</p>
<p><strong>HMODULE</strong> e <strong>HINSTANCE sono</strong> gli stessi nelle versioni correnti di Windows, ma rappresentavano elementi diversi nelle versioni a 16 bit Windows.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></td>
<td><p>Handle per un monitor di visualizzazione.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></td>
<td><p>Handle per una tavolozza.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></td>
<td><p>Handle per un <a href="/windows/desktop/gdi/pens">oggetto pen.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></td>
<td><p>Codici restituiti utilizzati dalle interfacce COM. Per altre informazioni, vedere <a href="/windows/desktop/com/structure-of-com-error-codes">Struttura dei codici di errore COM.</a> Per testare <strong>un valore HRESULT,</strong> usare le macro <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>e SUCCEEDED.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></td>
<td><p>Handle per <a href="/windows/desktop/gdi/regions">un'area</a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></td>
<td><p>Handle per una risorsa.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></td>
<td><p>Handle per una stringa DDE.</p>
<p>Questo tipo viene dichiarato in Ddeml.h come segue:</p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></td>
<td><p>Handle per una <a href="/windows/desktop/winstation/window-stations">stazione finestra.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></td>
<td><p>Handle per una <a href="/windows/desktop/winmsg/windows">finestra.</a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT"></span><span id="int"></span><strong>INT</strong></td>
<td><p>Intero con segno a 32 bit. L'intervallo è compreso tra -2147483648 e 2147483647 decimale.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></td>
<td><p>Tipo Signed Integer per la precisione del puntatore. Usare quando si esegue il cast di un puntatore a un integer per eseguire l'aritmetica dei puntatori.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64) 
 typedef __int64 INT_PTR; 
#else 
 typedef int INT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></td>
<td><p>Numero intero con segno a 8 bit.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></td>
<td><p>Intero con segno a 16 bit.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></td>
<td><p>Intero con segno a 32 bit. L'intervallo è compreso tra -2147483648 e 2147483647 decimale.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></td>
<td><p>Intero con segno a 64 bit. L'intervallo è compreso tra -9223372036854775808 e 9223372036854775807 decimale.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></td>
<td><p>Identificatore di lingua. Per altre informazioni, vedere <a href="/windows/desktop/Intl/language-identifiers">Identificatori di lingua.</a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></td>
<td><p>Identificatore delle impostazioni locali. Per altre informazioni, vedere <a href="/windows/desktop/Intl/locale-identifiers">Identificatori delle impostazioni locali.</a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></td>
<td><p>Tipo di informazioni sulle impostazioni locali. Per un elenco, vedere <a href="/windows/desktop/Intl/locale-information-constants">Costanti di informazioni sulle impostazioni locali</a>.</p>
<p>Questo tipo viene dichiarato in WinNls.h come indicato di seguito:</p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></td>
<td><p>Identificatore del gruppo di lingue. Per un elenco, vedere <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNls.h come indicato di seguito:</p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG"></span><span id="long"></span><strong>LUNGO</strong></td>
<td><p>Intero con segno a 32 bit. L'intervallo è compreso tra -2147483648 e 2147483647 decimale.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></td>
<td><p>Intero con segno a 64 bit. L'intervallo è compreso tra -9223372036854775808 e 9223372036854775807 decimale.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef __int64 LONGLONG; 
#else
 typedef double LONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></td>
<td><p>Tipo long con segno per la precisione del puntatore. Usare quando si esegue il cast di un puntatore a un oggetto long per eseguire operazioni aritmetiche del puntatore.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef __int64 LONG_PTR; 
#else
 typedef long LONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></td>
<td><p>Intero con segno a 32 bit. L'intervallo è compreso tra -2147483648 e 2147483647 decimale.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></td>
<td><p>Intero con segno a 64 bit. L'intervallo è compreso tra -9223372036854775808 e 9223372036854775807 decimale.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></td>
<td><p>Parametro del messaggio.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></td>
<td><p>Puntatore a un <a href="#bool"><strong>oggetto BOOL.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></td>
<td><p>Puntatore a un <a href="#byte"><strong>byte</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></td>
<td><p>Puntatore a un <a href="/windows/desktop/gdi/colorref"><strong>valore COLORREF.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></td>
<td><p>Puntatore a una stringa costante con terminazione Null di caratteri WINDOWS (ANSI) a 8 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></td>
<td><p><a href="#lpcwstr"><strong>LPCWSTR</strong></a> se <strong>è definito UNICODE,</strong> un <a href="#lpcstr"><strong>LPCSTR</strong></a> in caso contrario. Per altre informazioni, vedere Windows <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipi di dati per le stringhe</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR LPCTSTR; 
#else
 typedef LPCSTR LPCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></td>
<td><p>Puntatore a una costante di qualsiasi tipo.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></td>
<td><p>Puntatore a una stringa costante con terminazione Null di caratteri Unicode a 16 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></td>
<td><p>Puntatore a un <a href="#dword"><strong>valore DWORD</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></td>
<td><p>Puntatore a un <a href="#handle"><strong>handle</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></td>
<td><p>Puntatore a un <a href="#int"><strong>int</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></td>
<td><p>Puntatore a un <a href="#long"><strong>oggetto LONG.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></td>
<td><p>Puntatore a una stringa con terminazione Null di caratteri WINDOWS (ANSI) a 8 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></td>
<td><p>Un <a href="#lpwstr"><strong>LPWSTR</strong></a> se <strong>è definito UNICODE,</strong> un <a href="#lpstr"><strong>LPSTR in</strong></a> caso contrario. Per altre informazioni, vedere Windows <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipi di dati per le stringhe</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR LPTSTR;
#else
 typedef LPSTR LPTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></td>
<td><p>Puntatore a qualsiasi tipo.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></td>
<td><p>Puntatore a un <a href="#word"><strong>oggetto WORD.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></td>
<td><p>Puntatore a una stringa con terminazione Null di caratteri Unicode a 16 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></td>
<td><p>Risultato firmato dell'elaborazione del messaggio.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></td>
<td><p>Puntatore a un <a href="#bool"><strong>oggetto BOOL.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></td>
<td><p>Puntatore a un <a href="#boolean"><strong>booleano</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></td>
<td><p>Puntatore a un <a href="#byte"><strong>byte</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></td>
<td><p>Puntatore a un oggetto <a href="#char"><strong>CHAR.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></td>
<td><p>Puntatore a una stringa costante con terminazione Null di caratteri WINDOWS (ANSI) a 8 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></td>
<td><p><a href="#pcwstr"><strong>PCWSTR se</strong></a> <strong>è definito UNICODE,</strong> <a href="#pcstr"><strong>pcSTR</strong></a> in caso contrario. Per altre informazioni, vedere Windows <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipi di dati per le stringhe</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPCWSTR PCTSTR;
#else
 typedef LPCSTR PCTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></td>
<td><p>Puntatore a una stringa costante con terminazione Null di caratteri Unicode a 16 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere</a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></td>
<td><p>Puntatore a un <a href="#dword"><strong>valore DWORD</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></td>
<td><p>Puntatore a <a href="#dwordlong"><strong>un oggetto DWORDLONG</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></td>
<td><p>Puntatore a un <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></td>
<td><p>Puntatore a <a href="#dword32"><strong>un oggetto DWORD32.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></td>
<td><p>Puntatore a <a href="#dword64"><strong>un oggetto DWORD64.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></td>
<td><p>Puntatore a un <a href="#float"><strong>oggetto FLOAT.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></td>
<td><p>Puntatore a un <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef HALF_PTR *PHALF_PTR;
#else
 typedef HALF_PTR *PHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></td>
<td><p>Puntatore a un <a href="#handle"><strong>handle</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></td>
<td><p>Puntatore a un <a href="#hkey"><strong>oggetto HKEY</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT"></span><span id="pint"></span><strong>PINTA</strong></td>
<td><p>Puntatore a un <a href="#int"><strong>int</strong></a>.</p>
<p>Questo tipo viene dichiarato in WinDef.h come indicato di seguito:</p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></td>
<td><p>Puntatore a un <a href="#int_ptr"><strong>INT_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></td>
<td><p>Puntatore a un <a href="#int8"><strong>int8</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></td>
<td><p>Puntatore a un <a href="#int16"><strong>oggetto INT16.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></td>
<td><p>Puntatore a un <a href="#int32"><strong>int32</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></td>
<td><p>Puntatore a un <a href="#int64"><strong>int64</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></td>
<td><p>Puntatore a un <a href="#lcid"><strong>LCID.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></td>
<td><p>Puntatore a un <a href="#long"><strong>oggetto LONG.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONGLONG</strong></td>
<td><p>Puntatore a <a href="#longlong"><strong>longLONG.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></td>
<td><p>Puntatore a un <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></td>
<td><p>Puntatore a un <a href="#long32"><strong>oggetto LONG32.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></td>
<td><p>Puntatore a un <a href="#long64"><strong>long64</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></td>
<td><p>Puntatore a 32 bit. In un sistema a 32 bit si tratta di un puntatore nativo. In un sistema a 64 bit si tratta di un puntatore a 64 bit troncato.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
#define POINTER_32 __ptr32
#else
#define POINTER_32
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></td>
<td><p>Puntatore a 64 bit. In un sistema a 64 bit si tratta di un puntatore nativo. In un sistema a 32 bit si tratta di un puntatore a 32 bit esteso con segno.</p>
<p>Si noti che non è sicuro presupporre lo stato del bit del puntatore alto.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if (_MSC_VER >= 1300)
#define POINTER_64 __ptr64
#else
#define POINTER_64
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></td>
<td><p>Puntatore con segno.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></td>
<td><p>Puntatore senza segno.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></td>
<td><p>Puntatore a un <a href="#short"><strong>oggetto SHORT.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></td>
<td><p>Puntatore a un <a href="#size_t"><strong>SIZE_T</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></td>
<td><p>Puntatore a un <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></td>
<td><p>Puntatore a una stringa con terminazione Null di caratteri WINDOWS (ANSI) a 8 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere.</a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></td>
<td><p>Puntatore a un <a href="#tbyte"><strong>TBYTE.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></td>
<td><p>Puntatore a un <a href="#tchar"><strong>oggetto TCHAR.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></td>
<td><p><a href="#pwstr"><strong>PWSTR se</strong></a> <strong>è definito UNICODE;</strong> in caso <a href="#pstr"><strong>contrario, PSTR.</strong></a> Per altre informazioni, vedere <a href="/windows/desktop/Intl/windows-data-types-for-strings">l'Windows di dati per le stringhe.</a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef LPWSTR PTSTR;
#else typedef LPSTR PTSTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></td>
<td><p>Puntatore a un <a href="#uchar"><strong>UCHAR.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></td>
<td><p>Puntatore a un <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef UHALF_PTR *PUHALF_PTR;
#else
 typedef UHALF_PTR *PUHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></td>
<td><p>Puntatore a un <a href="#uint"><strong>UINT.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></td>
<td><p>Puntatore a un <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></td>
<td><p>Puntatore a un <a href="#uint8"><strong>UINT8.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></td>
<td><p>Puntatore a un <a href="#uint16"><strong>oggetto UINT16.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></td>
<td><p>Puntatore a un <a href="#uint32"><strong>oggetto UINT32.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></td>
<td><p>Puntatore a un <a href="#uint64"><strong>UINT64.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></td>
<td><p>Puntatore a un <a href="#ulong"><strong>ULONG.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></td>
<td><p>Puntatore a un <a href="#ulonglong"><strong>ULONGLONG.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></td>
<td><p>Puntatore a un <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></td>
<td><p>Puntatore a un <a href="#ulong32"><strong>ULONG32.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></td>
<td><p>Puntatore a un <a href="#ulong64"><strong>ULONG64.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></td>
<td><p>Puntatore a un <a href="#ushort"><strong>USHORT.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></td>
<td><p>Puntatore a qualsiasi tipo.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></td>
<td><p>Puntatore a un <a href="#wchar"><strong>oggetto WCHAR.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></td>
<td><p>Puntatore a un oggetto <a href="#word"><strong>WORD.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></td>
<td><p>Puntatore a una stringa con terminazione Null di caratteri Unicode a 16 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere.</a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></td>
<td><p>Intero senza segno a 64 bit.</p>
<p>Questo tipo viene dichiarato come segue:</p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></td>
<td><p>Handle per un database di Gestione controllo servizi. Per altre informazioni, vedere <a href="/windows/desktop/Services/scm-handles">Handle SCM.</a></p>
<p>Questo tipo viene dichiarato in WinSvc.h come indicato di seguito:</p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></td>
<td><p>Blocco a un database di Gestione controllo servizi. Per altre informazioni, vedere <a href="/windows/desktop/Services/scm-handles">Handle SCM.</a></p>
<p>Questo tipo viene dichiarato in WinSvc.h come indicato di seguito:</p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></td>
<td><p>Handle per un valore di stato del servizio. Per altre informazioni, vedere <a href="/windows/desktop/Services/scm-handles">Handle SCM.</a></p>
<p>Questo tipo viene dichiarato in WinSvc.h come indicato di seguito:</p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span id="SHORT"></span><span id="short"></span><strong>BREVE</strong></td>
<td><p>Intero a 16 bit. L'intervallo è compreso tra -32768 e 32767 decimale.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></td>
<td><p>Numero massimo di byte a cui un puntatore può puntare. Usare per un conteggio che deve estendersi all'intero intervallo di un puntatore.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></td>
<td><p>Versione firmata di <a href="#size_t"><strong>SIZE_T</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></td>
<td><p>WCHAR <a href="#wchar"><strong>se è</strong></a> <strong>definito UNICODE,</strong> char <a href="#char"><strong>in caso contrario.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TBYTE;
#else
 typedef unsigned char TBYTE;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></td>
<td><p>WCHAR <a href="#wchar"><strong>se è</strong></a> <strong>definito UNICODE,</strong> char <a href="#char"><strong>in caso contrario.</strong></a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef UNICODE
 typedef WCHAR TCHAR;
#else
 typedef char TCHAR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></td>
<td><p>Char senza <a href="#char"><strong>segno.</strong></a></p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></td>
<td><p>Oggetto senza <a href="#half_ptr"><strong>HALF_PTR</strong></a>. Usare all'interno di una struttura che contiene un puntatore e due campi piccoli.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#ifdef _WIN64
 typedef unsigned int UHALF_PTR;
#else
 typedef unsigned short UHALF_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></td>
<td><p>Unsigned <a href="#int"><strong>INT</strong></a>. L'intervallo è compreso tra 0 e 4294967295 decimale.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></td>
<td><p>Oggetto senza <a href="#int_ptr"><strong>segno INT_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 UINT_PTR;
#else
 typedef unsigned int UINT_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></td>
<td><p>Valore <a href="#int8"><strong>INT8 senza segno.</strong></a></p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></td>
<td><p>Valore <a href="#int16"><strong>INT16</strong></a>senza segno.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></td>
<td><p>Valore <a href="#int32"><strong>INT32 senza segno.</strong></a> L'intervallo è compreso tra 0 e 4294967295 decimale.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></td>
<td><p>Valore <a href="#int64"><strong>INT64 senza segno.</strong></a> L'intervallo è compreso tra 0 e 18446744073709551615 decimale.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></td>
<td><p>Long senza <a href="#long"><strong>segno.</strong></a> L'intervallo è compreso tra 0 e 4294967295 decimale.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></td>
<td><p>Intero senza segno a 64 bit. L'intervallo è compreso tra 0 e 18446744073709551615 decimale.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if !defined(_M_IX86)
 typedef unsigned __int64 ULONGLONG;
#else
 typedef double ULONGLONG;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></td>
<td><p>Oggetto senza <a href="#long_ptr"><strong>segno LONG_PTR</strong></a>.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>#if defined(_WIN64)
 typedef unsigned __int64 ULONG_PTR;
#else
 typedef unsigned long ULONG_PTR;
#endif</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></td>
<td><p>Long32 senza <a href="#long32"><strong>segno.</strong></a> L'intervallo è compreso tra 0 e 4294967295 decimale.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></td>
<td><p><a href="#long64"><strong>Long64 senza segno.</strong></a> L'intervallo è compreso tra 0 e 18446744073709551615 decimale.</p>
<p>Questo tipo viene dichiarato in BaseTsd.h come indicato di seguito:</p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></td>
<td><p>Stringa Unicode.</p>
<p>Questo tipo viene dichiarato in Talenl.h come indicato di seguito:</p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>typedef struct _UNICODE_STRING {
  USHORT  Length;
  USHORT  MaximumLength;
  PWSTR  Buffer;
} UNICODE_STRING;
typedef UNICODE_STRING *PUNICODE_STRING;
typedef const UNICODE_STRING *PCUNICODE_STRING;</code></pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></td>
<td><p>Oggetto SHORT senza <a href="#short"><strong>segno.</strong></a> L'intervallo è compreso tra 0 e 65535 decimali.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span id="USN"></span><span id="usn"></span><strong>USN</strong></td>
<td><p>Numero di sequenza di aggiornamento (USN).</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span id="VOID"></span><span id="void"></span><strong>VUOTO</strong></td>
<td><p>Qualsiasi tipo.</p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></td>
<td><p>Carattere Unicode a 16 bit. Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Set di caratteri usati dai tipi di carattere.</a></p>
<p>Questo tipo viene dichiarato in WinNT.h come indicato di seguito:</p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></td>
<td><p>Convenzione di chiamata per le funzioni di sistema.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>#define WINAPI __stdcall</code></p>
<p><strong>CALLBACK,</strong> <strong>WINAPI</strong>e <strong>APIENTRY</strong> vengono tutti usati per definire le funzioni con la __stdcall di chiamata. La maggior parte delle funzioni nell Windows API viene dichiarata usando <strong>WINAPI.</strong> È possibile usare <strong>CALLBACK per le</strong> funzioni di callback implementate per identificare la funzione come funzione di callback.</p></td>
</tr>
<tr class="even">
<td><span id="WORD"></span><span id="word"></span><strong>PAROLA</strong></td>
<td><p>Numero intero non firmato a 16 bit. L'intervallo è compreso tra 0 e 65535 decimali.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></td>
<td><p>Parametro del messaggio.</p>
<p>Questo tipo viene dichiarato in WinDef.h come segue:</p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop XP\]<br/>                                                                                                                                                                         |
| Server minimo supportato<br/> | Windows Solo app desktop server 2003 \[\]<br/>                                                                                                                                                                |
| Intestazione<br/>                   | <dl> <dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt> </dl> |
