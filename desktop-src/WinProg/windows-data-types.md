---
title: Tipi di dati di Windows (BaseTsd.h)
description: I tipi di dati supportati da Windows vengono utilizzati per definire i valori restituiti dalla funzione, i parametri della funzione e del messaggio e i membri della struttura.
ms.assetid: 4553cafc-450e-4493-a4d4-cb6e2f274d46
keywords:
- tipi di dati
- tipi di dati, Windows
- API Windows
- API Windows, tipi di dati
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
- PINT
- PINT_PTR
- PINT8
- PINT16
- PINT32
- PINT64
- PLCID
- PLONG
- PLONGLONG
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
ms.openlocfilehash: 9bf3a23e816a78f0dcae9c2fbd6e6979b936451c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400557"
---
# <a name="windows-data-types"></a><span data-ttu-id="938f8-280">Tipi di dati di Windows</span><span class="sxs-lookup"><span data-stu-id="938f8-280">Windows Data Types</span></span>

<span data-ttu-id="938f8-281">I tipi di dati supportati da Windows vengono utilizzati per definire i valori restituiti dalla funzione, i parametri della funzione e del messaggio e i membri della struttura.</span><span class="sxs-lookup"><span data-stu-id="938f8-281">The data types supported by Windows are used to define function return values, function and message parameters, and structure members.</span></span> <span data-ttu-id="938f8-282">Definiscono le dimensioni e il significato di questi elementi.</span><span class="sxs-lookup"><span data-stu-id="938f8-282">They define the size and meaning of these elements.</span></span> <span data-ttu-id="938f8-283">Per ulteriori informazioni sui tipi di dati C/C++ sottostanti, vedere [intervalli dei tipi di dati](/cpp/cpp/data-type-ranges?view=vs-2019).</span><span class="sxs-lookup"><span data-stu-id="938f8-283">For more information about the underlying C/C++ data types, see [Data Type Ranges](/cpp/cpp/data-type-ranges?view=vs-2019).</span></span>

<span data-ttu-id="938f8-284">La tabella seguente contiene i tipi seguenti: character, Integer, Boolean, Pointer e handle.</span><span class="sxs-lookup"><span data-stu-id="938f8-284">The following table contains the following types: character, integer, Boolean, pointer, and handle.</span></span> <span data-ttu-id="938f8-285">I tipi di carattere, Integer e Boolean sono comuni alla maggior parte dei compilatori C.</span><span class="sxs-lookup"><span data-stu-id="938f8-285">The character, integer, and Boolean types are common to most C compilers.</span></span> <span data-ttu-id="938f8-286">La maggior parte dei nomi di tipo puntatore inizia con un prefisso P o LP.</span><span class="sxs-lookup"><span data-stu-id="938f8-286">Most of the pointer-type names begin with a prefix of P or LP.</span></span> <span data-ttu-id="938f8-287">Gli handle fanno riferimento a una risorsa che è stata caricata in memoria.</span><span class="sxs-lookup"><span data-stu-id="938f8-287">Handles refer to a resource that has been loaded into memory.</span></span>

<span data-ttu-id="938f8-288">Per ulteriori informazioni sulla gestione di interi a 64 bit, vedere [grandi numeri interi](large-integers.md).</span><span class="sxs-lookup"><span data-stu-id="938f8-288">For more information about handling 64-bit integers, see [Large Integers](large-integers.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-289">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="938f8-289">Data type</span></span></th>
<th><span data-ttu-id="938f8-290">Descrizione</span><span class="sxs-lookup"><span data-stu-id="938f8-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="938f8-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-291"><span id="APIENTRY"></span><span id="apientry"></span><strong>APIENTRY</strong></span></span></td>
<td><span data-ttu-id="938f8-292">Convenzione di chiamata per le funzioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="938f8-292">The calling convention for system functions.</span></span><br/> <span data-ttu-id="938f8-293">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-293">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define APIENTRY WINAPI</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-294"><span id="ATOM"></span><span id="atom"></span><strong>ATOM</strong></span></span></td>
<td><span data-ttu-id="938f8-295">Un Atom.</span><span class="sxs-lookup"><span data-stu-id="938f8-295">An atom.</span></span> <span data-ttu-id="938f8-296">Per ulteriori informazioni, vedere <a href="/windows/desktop/dataxchg/about-atom-tables">informazioni sulle tabelle Atom</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-296">For more information, see <a href="/windows/desktop/dataxchg/about-atom-tables">About Atom Tables</a>.</span></span><br/> <span data-ttu-id="938f8-297">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-297">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef WORD ATOM;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-298"><span id="BOOL"></span><span id="bool"></span><strong>BOOL</strong></span></span></td>
<td><span data-ttu-id="938f8-299">Una variabile booleana (deve essere <strong>true</strong> o <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="938f8-299">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="938f8-300">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-300">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef int BOOL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-301"><span id="BOOLEAN"></span><span id="boolean"></span><strong>BOOLEAN</strong></span></span></td>
<td><span data-ttu-id="938f8-302">Una variabile booleana (deve essere <strong>true</strong> o <strong>false</strong>).</span><span class="sxs-lookup"><span data-stu-id="938f8-302">A Boolean variable (should be <strong>TRUE</strong> or <strong>FALSE</strong>).</span></span><br/> <span data-ttu-id="938f8-303">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-303">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef BYTE BOOLEAN;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-304"><span id="BYTE"></span><span id="byte"></span><strong>BYTE</strong></span></span></td>
<td><span data-ttu-id="938f8-305">Byte (8 bit).</span><span class="sxs-lookup"><span data-stu-id="938f8-305">A byte (8 bits).</span></span><br/> <span data-ttu-id="938f8-306">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-306">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef unsigned char BYTE;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-307"><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-307"><span id="CALLBACK"></span><span id="callback"></span><strong>CALLBACK</strong></span></span></td>
<td><span data-ttu-id="938f8-308">Convenzione di chiamata per le funzioni di callback.</span><span class="sxs-lookup"><span data-stu-id="938f8-308">The calling convention for callback functions.</span></span><br/> <span data-ttu-id="938f8-309">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-309">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CALLBACK __stdcall</code><br/> <span data-ttu-id="938f8-310"><strong>Callback</strong>, <strong>WINAPI</strong>e <strong>APIENTRY</strong> vengono utilizzati tutti per definire funzioni con la convenzione di chiamata __stdcall.</span><span class="sxs-lookup"><span data-stu-id="938f8-310"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="938f8-311">La maggior parte delle funzioni nell'API Windows viene dichiarata usando <strong>WINAPI</strong>.</span><span class="sxs-lookup"><span data-stu-id="938f8-311">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="938f8-312">È possibile utilizzare <strong>callback</strong> per le funzioni di callback implementate per identificare la funzione come funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="938f8-312">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-313"><span id="CCHAR"></span><span id="cchar"></span><strong>CCHAR</strong></span></span></td>
<td><span data-ttu-id="938f8-314">Un carattere Windows a 8 bit (ANSI).</span><span class="sxs-lookup"><span data-stu-id="938f8-314">An 8-bit Windows (ANSI) character.</span></span><br/> <span data-ttu-id="938f8-315">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-315">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CCHAR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-316"><span id="CHAR"></span><span id="char"></span><strong>CHAR</strong></span></span></td>
<td><span data-ttu-id="938f8-317">Un carattere Windows a 8 bit (ANSI).</span><span class="sxs-lookup"><span data-stu-id="938f8-317">An 8-bit Windows (ANSI) character.</span></span> <span data-ttu-id="938f8-318">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-318">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span><br/> <span data-ttu-id="938f8-319">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-319">This type is declared in WinNT.h as follows:</span></span><br/> <code>typedef char CHAR;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-320"><span id="COLORREF"></span><span id="colorref"></span><strong>COLORREF</strong></span></span></td>
<td><span data-ttu-id="938f8-321">Il valore di colore rosso, verde, blu (RGB) (32 bit).</span><span class="sxs-lookup"><span data-stu-id="938f8-321">The red, green, blue (RGB) color value (32 bits).</span></span> <span data-ttu-id="938f8-322">Per informazioni su questo tipo, vedere <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="938f8-322">See <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> for information on this type.</span></span><br/> <span data-ttu-id="938f8-323">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-323">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef DWORD COLORREF;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-324"><span id="CONST"></span><span id="const"></span><strong>CONST</strong></span></span></td>
<td><span data-ttu-id="938f8-325">Variabile il cui valore deve rimanere costante durante l'esecuzione.</span><span class="sxs-lookup"><span data-stu-id="938f8-325">A variable whose value is to remain constant during execution.</span></span> <br/> <span data-ttu-id="938f8-326">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-326">This type is declared in WinDef.h as follows:</span></span><br/> <code>#define CONST const</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-327"><span id="DWORD"></span><span id="dword"></span><strong>DWORD</strong></span></span></td>
<td><span data-ttu-id="938f8-328">Intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-328">A 32-bit unsigned integer.</span></span> <span data-ttu-id="938f8-329">L'intervallo è compreso tra 0 e 4294967295 decimale.</span><span class="sxs-lookup"><span data-stu-id="938f8-329">The range is 0 through 4294967295 decimal.</span></span><br/> <span data-ttu-id="938f8-330">Questo tipo viene dichiarato in IntSafe. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-330">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned long DWORD;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-331"><span id="DWORDLONG"></span><span id="dwordlong"></span><strong>DWORDLONG</strong></span></span></td>
<td><span data-ttu-id="938f8-332">Intero senza segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-332">A 64-bit unsigned integer.</span></span> <span data-ttu-id="938f8-333">L'intervallo è compreso tra 0 e 18.446.744.073.709.551.615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-333">The range is 0 through 18446744073709551615 decimal.</span></span><br/> <span data-ttu-id="938f8-334">Questo tipo viene dichiarato in IntSafe. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-334">This type is declared in IntSafe.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORDLONG;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-335"><span id="DWORD_PTR"></span><span id="dword_ptr"></span><strong>DWORD_PTR</strong></span></span></td>
<td><span data-ttu-id="938f8-336">Tipo long senza segno per la precisione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-336">An unsigned long type for pointer precision.</span></span> <span data-ttu-id="938f8-337">Usare quando si esegue il cast di un puntatore a un tipo Long per eseguire l'aritmetica del puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-337">Use when casting a pointer to a long type to perform pointer arithmetic.</span></span> <span data-ttu-id="938f8-338">(Anche comunemente usato per i parametri generali a 32 bit che sono stati estesi a 64 bit in Windows a 64 bit).</span><span class="sxs-lookup"><span data-stu-id="938f8-338">(Also commonly used for general 32-bit parameters that have been extended to 64 bits in 64-bit Windows.)</span></span><br/> <span data-ttu-id="938f8-339">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-339">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef ULONG_PTR DWORD_PTR;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-340"><span id="DWORD32"></span><span id="dword32"></span><strong>DWORD32</strong></span></span></td>
<td><span data-ttu-id="938f8-341">Intero senza segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-341">A 32-bit unsigned integer.</span></span><br/> <span data-ttu-id="938f8-342">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-342">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned int DWORD32;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-343"><span id="DWORD64"></span><span id="dword64"></span><strong>DWORD64</strong></span></span></td>
<td><span data-ttu-id="938f8-344">Intero senza segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-344">A 64-bit unsigned integer.</span></span><br/> <span data-ttu-id="938f8-345">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-345">This type is declared in BaseTsd.h as follows:</span></span><br/> <code>typedef unsigned __int64 DWORD64;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOAT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-346"><span id="FLOAT"></span><span id="float"></span><strong>FLOAT</strong></span></span></td>
<td><span data-ttu-id="938f8-347">Variabile a virgola mobile.</span><span class="sxs-lookup"><span data-stu-id="938f8-347">A floating-point variable.</span></span><br/> <span data-ttu-id="938f8-348">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-348">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef float FLOAT;</code><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-349"><span id="HACCEL"></span><span id="haccel"></span><strong>HACCEL</strong></span></span></td>
<td><span data-ttu-id="938f8-350">Handle per una <a href="/windows/desktop/menurc/keyboard-accelerators">tabella di tasti di scelta rapida</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-350">A handle to an <a href="/windows/desktop/menurc/keyboard-accelerators">accelerator table</a>.</span></span><br/> <span data-ttu-id="938f8-351">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-351">This type is declared in WinDef.h as follows:</span></span><br/> <code>typedef HANDLE HACCEL;</code><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-352"><span id="HALF_PTR"></span><span id="half_ptr"></span><strong>HALF_PTR</strong></span></span></td>
<td><span data-ttu-id="938f8-353">Metà delle dimensioni di un puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-353">Half the size of a pointer.</span></span> <span data-ttu-id="938f8-354">Utilizzare all'interno di una struttura che contiene un puntatore e due campi di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="938f8-354">Use within a structure that contains a pointer and two small fields.</span></span><br/> <span data-ttu-id="938f8-355">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-355">This type is declared in BaseTsd.h as follows:</span></span><br/> <span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-356">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-356">C++</span></span></th>
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
<td><span data-ttu-id="938f8-357"><span id="HANDLE"></span><span id="handle"></span><strong>GESTIRE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-357"><span id="HANDLE"></span><span id="handle"></span><strong>HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-358">Handle per un oggetto.</span><span class="sxs-lookup"><span data-stu-id="938f8-358">A handle to an object.</span></span></p>
<p><span data-ttu-id="938f8-359">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-359">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PVOID HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-360"><span id="HBITMAP"></span><span id="hbitmap"></span><strong>HBITMAP</strong></span></span></td>
<td><p><span data-ttu-id="938f8-361">Handle per una <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-361">A handle to a <a href="/windows/desktop/gdi/bitmaps">bitmap</a>.</span></span></p>
<p><span data-ttu-id="938f8-362">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-362">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBITMAP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-363"><span id="HBRUSH"></span><span id="hbrush"></span><strong>HBRUSH</strong></span></span></td>
<td><p><span data-ttu-id="938f8-364">Handle per un <a href="/windows/desktop/gdi/brushes">pennello</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-364">A handle to a <a href="/windows/desktop/gdi/brushes">brush</a>.</span></span></p>
<p><span data-ttu-id="938f8-365">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-365">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HBRUSH;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-366"><span id="HCOLORSPACE"></span><span id="hcolorspace"></span><strong>HCOLORSPACE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-367">Handle per uno <a href="/previous-versions//dd316799(v=vs.85)">spazio colore</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-367">A handle to a <a href="/previous-versions//dd316799(v=vs.85)">color space</a>.</span></span></p>
<p><span data-ttu-id="938f8-368">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-368">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HCOLORSPACE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-369"><span id="HCONV"></span><span id="hconv"></span><strong>HCONV</strong></span></span></td>
<td><p><span data-ttu-id="938f8-370">Handle per una conversazione DDE (Dynamic Data Exchange).</span><span class="sxs-lookup"><span data-stu-id="938f8-370">A handle to a dynamic data exchange (DDE) conversation.</span></span></p>
<p><span data-ttu-id="938f8-371">Questo tipo viene dichiarato in DDEML. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-371">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONV;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-372"><span id="HCONVLIST"></span><span id="hconvlist"></span><strong>HCONVLIST</strong></span></span></td>
<td><p><span data-ttu-id="938f8-373">Handle per un elenco di conversazioni DDE.</span><span class="sxs-lookup"><span data-stu-id="938f8-373">A handle to a DDE conversation list.</span></span></p>
<p><span data-ttu-id="938f8-374">Questo tipo viene dichiarato in DDEML. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-374">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HCONVLIST;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-375"><span id="HCURSOR"></span><span id="hcursor"></span><strong>HCURSOR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-376">Handle per un <a href="/windows/desktop/menurc/cursors">cursore</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-376">A handle to a <a href="/windows/desktop/menurc/cursors">cursor</a>.</span></span></p>
<p><span data-ttu-id="938f8-377">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-377">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HICON HCURSOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-378"><span id="HDC"></span><span id="hdc"></span><strong>HDC</strong></span></span></td>
<td><p><span data-ttu-id="938f8-379">Handle per un <a href="/windows/desktop/gdi/device-context-types">contesto di periferica</a> (DC).</span><span class="sxs-lookup"><span data-stu-id="938f8-379">A handle to a <a href="/windows/desktop/gdi/device-context-types">device context</a> (DC).</span></span></p>
<p><span data-ttu-id="938f8-380">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-380">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-381"><span id="HDDEDATA"></span><span id="hddedata"></span><strong>HDDEDATA</strong></span></span></td>
<td><p><span data-ttu-id="938f8-382">Handle per i dati DDE.</span><span class="sxs-lookup"><span data-stu-id="938f8-382">A handle to DDE data.</span></span></p>
<p><span data-ttu-id="938f8-383">Questo tipo viene dichiarato in DDEML. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-383">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HDDEDATA;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-384"><span id="HDESK"></span><span id="hdesk"></span><strong>HDESK</strong></span></span></td>
<td><p><span data-ttu-id="938f8-385">Handle per un <a href="/windows/desktop/winstation/desktops">Desktop</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-385">A handle to a <a href="/windows/desktop/winstation/desktops">desktop</a>.</span></span></p>
<p><span data-ttu-id="938f8-386">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-386">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HDESK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-387"><span id="HDROP"></span><span id="hdrop"></span><strong>HDROP</strong></span></span></td>
<td><p><span data-ttu-id="938f8-388">Handle per una struttura di rilascio interna.</span><span class="sxs-lookup"><span data-stu-id="938f8-388">A handle to an internal drop structure.</span></span></p>
<p><span data-ttu-id="938f8-389">Questo tipo viene dichiarato in ShellApi. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-389">This type is declared in ShellApi.h as follows:</span></span></p>
<p><code>typedef HANDLE HDROP;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-390"><span id="HDWP"></span><span id="hdwp"></span><strong>HDWP</strong></span></span></td>
<td><p><span data-ttu-id="938f8-391">Handle per una struttura di posizione della finestra posticipata.</span><span class="sxs-lookup"><span data-stu-id="938f8-391">A handle to a deferred window position structure.</span></span></p>
<p><span data-ttu-id="938f8-392">Questo tipo viene dichiarato in WinUser. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-392">This type is declared in WinUser.h as follows:</span></span></p>
<p><code>typedef HANDLE HDWP;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-393"><span id="HENHMETAFILE"></span><span id="henhmetafile"></span><strong>HENHMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-394">Handle per un <a href="/windows/desktop/gdi/metafiles">metafile avanzato</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-394">A handle to an <a href="/windows/desktop/gdi/metafiles">enhanced metafile</a>.</span></span></p>
<p><span data-ttu-id="938f8-395">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-395">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HENHMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-396"><span id="HFILE"></span><span id="hfile"></span><strong>HFILE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-397">Handle per un file aperto da <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, non <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-397">A handle to a file opened by <a href="/windows/desktop/api/winbase/nf-winbase-openfile"><strong>OpenFile</strong></a>, not <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea"><strong>CreateFile</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-398">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-398">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int HFILE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-399"><span id="HFONT"></span><span id="hfont"></span><strong>HFONT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-400">Handle per un <a href="/windows/desktop/gdi/about-fonts">tipo di carattere</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-400">A handle to a <a href="/windows/desktop/gdi/about-fonts">font</a>.</span></span></p>
<p><span data-ttu-id="938f8-401">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-401">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HFONT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-402"><span id="HGDIOBJ"></span><span id="hgdiobj"></span><strong>HGDIOBJ</strong></span></span></td>
<td><p><span data-ttu-id="938f8-403">Handle per un oggetto GDI.</span><span class="sxs-lookup"><span data-stu-id="938f8-403">A handle to a GDI object.</span></span></p>
<p><span data-ttu-id="938f8-404">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-404">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGDIOBJ;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-405"><span id="HGLOBAL"></span><span id="hglobal"></span><strong>HGLOBAL</strong></span></span></td>
<td><p><span data-ttu-id="938f8-406">Handle per un blocco di memoria globale.</span><span class="sxs-lookup"><span data-stu-id="938f8-406">A handle to a global memory block.</span></span></p>
<p><span data-ttu-id="938f8-407">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-407">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HGLOBAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-408"><span id="HHOOK"></span><span id="hhook"></span><strong>HHOOK</strong></span></span></td>
<td><p><span data-ttu-id="938f8-409">Handle per un <a href="/windows/desktop/winmsg/hooks">hook</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-409">A handle to a <a href="/windows/desktop/winmsg/hooks">hook</a>.</span></span></p>
<p><span data-ttu-id="938f8-410">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-410">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HHOOK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-411"><span id="HICON"></span><span id="hicon"></span><strong>HICON</strong></span></span></td>
<td><p><span data-ttu-id="938f8-412">Handle per un' <a href="/windows/desktop/menurc/icons">icona</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-412">A handle to an <a href="/windows/desktop/menurc/icons">icon</a>.</span></span></p>
<p><span data-ttu-id="938f8-413">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-413">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HICON;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-414"><span id="HINSTANCE"></span><span id="hinstance"></span><strong>HINSTANCE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-415">Handle per un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="938f8-415">A handle to an instance.</span></span> <span data-ttu-id="938f8-416">Si tratta dell'indirizzo di base del modulo in memoria.</span><span class="sxs-lookup"><span data-stu-id="938f8-416">This is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="938f8-417"><strong>Hmodule</strong> e <strong>HINSTANCE</strong> sono gli stessi oggi, ma sono stati rappresentati diversi in Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-417"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same today, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="938f8-418">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-418">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HINSTANCE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-419"><span id="HKEY"></span><span id="hkey"></span><strong>HKEY</strong></span></span></td>
<td><p><span data-ttu-id="938f8-420">Handle per una chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="938f8-420">A handle to a registry key.</span></span></p>
<p><span data-ttu-id="938f8-421">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-421">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKEY;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-422"><span id="HKL"></span><span id="hkl"></span><strong>HKL</strong></span></span></td>
<td><p><span data-ttu-id="938f8-423">Identificatore delle impostazioni locali di input.</span><span class="sxs-lookup"><span data-stu-id="938f8-423">An input locale identifier.</span></span></p>
<p><span data-ttu-id="938f8-424">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-424">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HKL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-425"><span id="HLOCAL"></span><span id="hlocal"></span><strong>HLOCAL</strong></span></span></td>
<td><p><span data-ttu-id="938f8-426">Handle per un blocco di memoria locale.</span><span class="sxs-lookup"><span data-stu-id="938f8-426">A handle to a local memory block.</span></span></p>
<p><span data-ttu-id="938f8-427">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-427">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HLOCAL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-428"><span id="HMENU"></span><span id="hmenu"></span><strong>HMENU</strong></span></span></td>
<td><p><span data-ttu-id="938f8-429">Handle per un <a href="/windows/desktop/menurc/menus">menu</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-429">A handle to a <a href="/windows/desktop/menurc/menus">menu</a>.</span></span></p>
<p><span data-ttu-id="938f8-430">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-430">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMENU;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-431"><span id="HMETAFILE"></span><span id="hmetafile"></span><strong>HMETAFILE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-432">Handle per un <a href="/windows/desktop/gdi/metafiles">metafile</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-432">A handle to a <a href="/windows/desktop/gdi/metafiles">metafile</a>.</span></span></p>
<p><span data-ttu-id="938f8-433">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-433">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HMETAFILE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-434"><span id="HMODULE"></span><span id="hmodule"></span><strong>HMODULE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-435">Handle per un modulo.</span><span class="sxs-lookup"><span data-stu-id="938f8-435">A handle to a module.</span></span> <span data-ttu-id="938f8-436">È l'indirizzo di base del modulo in memoria.</span><span class="sxs-lookup"><span data-stu-id="938f8-436">The is the base address of the module in memory.</span></span></p>
<p><span data-ttu-id="938f8-437"><strong>Hmodule</strong> e <strong>HINSTANCE</strong> sono uguali nelle versioni correnti di Windows, ma sono rappresentati in Windows a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-437"><strong>HMODULE</strong> and <strong>HINSTANCE</strong> are the same in current versions of Windows, but represented different things in 16-bit Windows.</span></span></p>
<p><span data-ttu-id="938f8-438">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-438">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HINSTANCE HMODULE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-439"><span id="HMONITOR"></span><span id="hmonitor"></span><strong>HMONITOR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-440">Handle per un monitor di visualizzazione.</span><span class="sxs-lookup"><span data-stu-id="938f8-440">A handle to a display monitor.</span></span></p>
<p><span data-ttu-id="938f8-441">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-441">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>if(WINVER >= 0x0500) typedef HANDLE HMONITOR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-442"><span id="HPALETTE"></span><span id="hpalette"></span><strong>HPALETTE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-443">Handle per una tavolozza.</span><span class="sxs-lookup"><span data-stu-id="938f8-443">A handle to a palette.</span></span></p>
<p><span data-ttu-id="938f8-444">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-444">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPALETTE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-445"><span id="HPEN"></span><span id="hpen"></span><strong>HPEN</strong></span></span></td>
<td><p><span data-ttu-id="938f8-446">Handle per una <a href="/windows/desktop/gdi/pens">penna</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-446">A handle to a <a href="/windows/desktop/gdi/pens">pen</a>.</span></span></p>
<p><span data-ttu-id="938f8-447">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-447">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HPEN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-448"><span id="HRESULT"></span><span id="hresult"></span><strong>HRESULT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-449">Codici restituiti usati dalle interfacce COM.</span><span class="sxs-lookup"><span data-stu-id="938f8-449">The return codes used by COM interfaces.</span></span> <span data-ttu-id="938f8-450">Per ulteriori informazioni, vedere <a href="/windows/desktop/com/structure-of-com-error-codes">la pagina relativa alla struttura dei codici di errore com</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-450">For more information, see <a href="/windows/desktop/com/structure-of-com-error-codes">Structure of the COM Error Codes</a>.</span></span> <span data-ttu-id="938f8-451">Per testare un valore <strong>HRESULT</strong> , usare le macro <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>failed</strong></a> e <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>succeeded</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="938f8-451">To test an <strong>HRESULT</strong> value, use the <a href="/windows/desktop/api/winerror/nf-winerror-failed"><strong>FAILED</strong></a> and <a href="/windows/desktop/api/winerror/nf-winerror-succeeded"><strong>SUCCEEDED</strong></a> macros.</span></span></p>
<p><span data-ttu-id="938f8-452">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-452">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG HRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-453"><span id="HRGN"></span><span id="hrgn"></span><strong>HRGN</strong></span></span></td>
<td><p><span data-ttu-id="938f8-454">Handle per un' <a href="/windows/desktop/gdi/regions">area</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-454">A handle to a <a href="/windows/desktop/gdi/regions">region</a>.</span></span></p>
<p><span data-ttu-id="938f8-455">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-455">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRGN;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-456"><span id="HRSRC"></span><span id="hrsrc"></span><strong>HRSRC</strong></span></span></td>
<td><p><span data-ttu-id="938f8-457">Handle per una risorsa.</span><span class="sxs-lookup"><span data-stu-id="938f8-457">A handle to a resource.</span></span></p>
<p><span data-ttu-id="938f8-458">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-458">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HRSRC;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-459"><span id="HSZ"></span><span id="hsz"></span><strong>HSZ</strong></span></span></td>
<td><p><span data-ttu-id="938f8-460">Handle per una stringa DDE.</span><span class="sxs-lookup"><span data-stu-id="938f8-460">A handle to a DDE string.</span></span></p>
<p><span data-ttu-id="938f8-461">Questo tipo viene dichiarato in DDEML. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-461">This type is declared in Ddeml.h as follows:</span></span></p>
<p><code>typedef HANDLE HSZ;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-462"><span id="HWINSTA"></span><span id="hwinsta"></span><strong>HWINSTA</strong></span></span></td>
<td><p><span data-ttu-id="938f8-463">Handle per una <a href="/windows/desktop/winstation/window-stations">stazione di finestra</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-463">A handle to a <a href="/windows/desktop/winstation/window-stations">window station</a>.</span></span></p>
<p><span data-ttu-id="938f8-464">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-464">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE WINSTA;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-465"><span id="HWND"></span><span id="hwnd"></span><strong>HWND</strong></span></span></td>
<td><p><span data-ttu-id="938f8-466">Handle per una <a href="/windows/desktop/winmsg/windows">finestra</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-466">A handle to a <a href="/windows/desktop/winmsg/windows">window</a>.</span></span></p>
<p><span data-ttu-id="938f8-467">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-467">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE HWND;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-468"><span id="INT"></span><span id="int"></span><strong>INT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-469">Intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-469">A 32-bit signed integer.</span></span> <span data-ttu-id="938f8-470">L'intervallo è compreso tra-2147483648 e 2147483647 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-470">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="938f8-471">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-471">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int INT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-472"><span id="INT_PTR"></span><span id="int_ptr"></span><strong>INT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-473">Tipo signed integer per la precisione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-473">A signed integer type for pointer precision.</span></span> <span data-ttu-id="938f8-474">Usare quando si esegue il cast di un puntatore a un Integer per eseguire l'aritmetica del puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-474">Use when casting a pointer to an integer to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="938f8-475">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-475">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-476">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-476">C++</span></span></th>
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
<td><span data-ttu-id="938f8-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-477"><span id="INT8"></span><span id="int8"></span><strong>INT8</strong></span></span></td>
<td><p><span data-ttu-id="938f8-478">Numero intero con segno a 8 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-478">An 8-bit signed integer.</span></span></p>
<p><span data-ttu-id="938f8-479">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-479">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed char INT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-480"><span id="INT16"></span><span id="int16"></span><strong>INT16</strong></span></span></td>
<td><p><span data-ttu-id="938f8-481">Intero con segno a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-481">A 16-bit signed integer.</span></span></p>
<p><span data-ttu-id="938f8-482">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-482">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed short INT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-483"><span id="INT32"></span><span id="int32"></span><strong>INT32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-484">Intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-484">A 32-bit signed integer.</span></span> <span data-ttu-id="938f8-485">L'intervallo è compreso tra-2147483648 e 2147483647 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-485">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="938f8-486">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-486">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int INT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-487"><span id="INT64"></span><span id="int64"></span><strong>INT64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-488">Intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-488">A 64-bit signed integer.</span></span> <span data-ttu-id="938f8-489">L'intervallo è da-9.223.372.036.854.775.808 a 9223372036854775807 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-489">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="938f8-490">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-490">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed __int64 INT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-491"><span id="LANGID"></span><span id="langid"></span><strong>LANGID</strong></span></span></td>
<td><p><span data-ttu-id="938f8-492">Identificatore di lingua.</span><span class="sxs-lookup"><span data-stu-id="938f8-492">A language identifier.</span></span> <span data-ttu-id="938f8-493">Per ulteriori informazioni, vedere <a href="/windows/desktop/Intl/language-identifiers">identificatori di lingua</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-493">For more information, see <a href="/windows/desktop/Intl/language-identifiers">Language Identifiers</a>.</span></span></p>
<p><span data-ttu-id="938f8-494">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-494">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WORD LANGID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-495"><span id="LCID"></span><span id="lcid"></span><strong>LCID</strong></span></span></td>
<td><p><span data-ttu-id="938f8-496">Identificatore delle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="938f8-496">A locale identifier.</span></span> <span data-ttu-id="938f8-497">Per ulteriori informazioni, vedere <a href="/windows/desktop/Intl/locale-identifiers">identificatori delle impostazioni locali</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-497">For more information, see <a href="/windows/desktop/Intl/locale-identifiers">Locale Identifiers</a>.</span></span></p>
<p><span data-ttu-id="938f8-498">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-498">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORD LCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-499"><span id="LCTYPE"></span><span id="lctype"></span><strong>LCTYPE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-500">Tipo di informazioni sulle impostazioni locali.</span><span class="sxs-lookup"><span data-stu-id="938f8-500">A locale information type.</span></span> <span data-ttu-id="938f8-501">Per un elenco, vedere <a href="/windows/desktop/Intl/locale-information-constants">costanti di informazioni sulle impostazioni locali</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-501">For a list, see <a href="/windows/desktop/Intl/locale-information-constants">Locale Information Constants</a>.</span></span></p>
<p><span data-ttu-id="938f8-502">Questo tipo viene dichiarato in WinNls. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-502">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LCTYPE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-503"><span id="LGRPID"></span><span id="lgrpid"></span><strong>LGRPID</strong></span></span></td>
<td><p><span data-ttu-id="938f8-504">Identificatore del gruppo di lingue.</span><span class="sxs-lookup"><span data-stu-id="938f8-504">A language group identifier.</span></span> <span data-ttu-id="938f8-505">Per un elenco, vedere <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-505">For a list, see <a href="/windows/desktop/api/winnls/nf-winnls-enumlanguagegrouplocalesa"><strong>EnumLanguageGroupLocales</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-506">Questo tipo viene dichiarato in WinNls. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-506">This type is declared in WinNls.h as follows:</span></span></p>
<p><code>typedef DWORD LGRPID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-507"><span id="LONG"></span><span id="long"></span><strong>LUNGO</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-507"><span id="LONG"></span><span id="long"></span><strong>LONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-508">Intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-508">A 32-bit signed integer.</span></span> <span data-ttu-id="938f8-509">L'intervallo è compreso tra-2147483648 e 2147483647 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-509">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="938f8-510">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-510">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef long LONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-511"><span id="LONGLONG"></span><span id="longlong"></span><strong>LONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-512">Intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-512">A 64-bit signed integer.</span></span> <span data-ttu-id="938f8-513">L'intervallo è da-9.223.372.036.854.775.808 a 9223372036854775807 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-513">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="938f8-514">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-514">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-515">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-515">C++</span></span></th>
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
<td><span data-ttu-id="938f8-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-516"><span id="LONG_PTR"></span><span id="long_ptr"></span><strong>LONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-517">Tipo Long con segno per la precisione del puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-517">A signed long type for pointer precision.</span></span> <span data-ttu-id="938f8-518">Usare quando si esegue il cast di un puntatore a un oggetto Long per eseguire l'aritmetica del puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-518">Use when casting a pointer to a long to perform pointer arithmetic.</span></span></p>
<p><span data-ttu-id="938f8-519">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-519">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-520">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-520">C++</span></span></th>
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
<td><span data-ttu-id="938f8-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-521"><span id="LONG32"></span><span id="long32"></span><strong>LONG32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-522">Intero con segno a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-522">A 32-bit signed integer.</span></span> <span data-ttu-id="938f8-523">L'intervallo è compreso tra-2147483648 e 2147483647 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-523">The range is -2147483648 through 2147483647 decimal.</span></span></p>
<p><span data-ttu-id="938f8-524">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-524">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef signed int LONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-525"><span id="LONG64"></span><span id="long64"></span><strong>LONG64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-526">Intero con segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-526">A 64-bit signed integer.</span></span> <span data-ttu-id="938f8-527">L'intervallo è da-9.223.372.036.854.775.808 a 9223372036854775807 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-527">The range is -9223372036854775808 through 9223372036854775807 decimal.</span></span></p>
<p><span data-ttu-id="938f8-528">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-528">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef __int64 LONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-529"><span id="LPARAM"></span><span id="lparam"></span><strong>LPARAM</strong></span></span></td>
<td><p><span data-ttu-id="938f8-530">Parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="938f8-530">A message parameter.</span></span></p>
<p><span data-ttu-id="938f8-531">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-531">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LPARAM;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-532"><span id="LPBOOL"></span><span id="lpbool"></span><strong>LPBOOL</strong></span></span></td>
<td><p><span data-ttu-id="938f8-533">Puntatore a un <a href="#bool"><strong>bool</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-533">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-534">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-534">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL far *LPBOOL;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-535"><span id="LPBYTE"></span><span id="lpbyte"></span><strong>LPBYTE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-536">Puntatore a un <a href="#byte"><strong>byte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-536">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-537">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-537">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE far *LPBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-538"><span id="LPCOLORREF"></span><span id="lpcolorref"></span><strong>LPCOLORREF</strong></span></span></td>
<td><p><span data-ttu-id="938f8-539">Puntatore a un valore <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="938f8-539">A pointer to a <a href="/windows/desktop/gdi/colorref"><strong>COLORREF</strong></a> value.</span></span></p>
<p><span data-ttu-id="938f8-540">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-540">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPCOLORREF;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-541"><span id="LPCSTR"></span><span id="lpcstr"></span><strong>LPCSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-542">Puntatore a una stringa costante con terminazione null di caratteri di Windows a 8 bit (ANSI).</span><span class="sxs-lookup"><span data-stu-id="938f8-542">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="938f8-543">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-543">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-544">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-544">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef __nullterminated CONST CHAR *LPCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-545"><span id="LPCTSTR"></span><span id="lpctstr"></span><strong>LPCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-546">Un <a href="#lpcwstr"><strong>LPCWSTR</strong></a> se è definito <strong>Unicode</strong> , un <a href="#lpcstr"><strong>LPCSTR</strong></a> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="938f8-546">An <a href="#lpcwstr"><strong>LPCWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpcstr"><strong>LPCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="938f8-547">Per ulteriori informazioni, vedere <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipi di dati di Windows per le stringhe</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-547">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="938f8-548">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-548">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-549">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-549">C++</span></span></th>
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
<td><span data-ttu-id="938f8-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-550"><span id="LPCVOID"></span><span id="lpcvoid"></span><strong>LPCVOID</strong></span></span></td>
<td><p><span data-ttu-id="938f8-551">Puntatore a una costante di qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="938f8-551">A pointer to a constant of any type.</span></span></p>
<p><span data-ttu-id="938f8-552">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-552">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef CONST void *LPCVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-553"><span id="LPCWSTR"></span><span id="lpcwstr"></span><strong>LPCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-554">Puntatore a una stringa costante con terminazione null di caratteri Unicode a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-554">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="938f8-555">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-555">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-556">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-556">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *LPCWSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-557"><span id="LPDWORD"></span><span id="lpdword"></span><strong>LPDWORD</strong></span></span></td>
<td><p><span data-ttu-id="938f8-558">Puntatore a un <a href="#dword"><strong>valore DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-558">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-559">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-559">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *LPDWORD;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-560"><span id="LPHANDLE"></span><span id="lphandle"></span><strong>LPHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-561">Puntatore a un <a href="#handle"><strong>handle</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-561">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-562">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-562">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HANDLE *LPHANDLE;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-563"><span id="LPINT"></span><span id="lpint"></span><strong>LPINT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-564">Puntatore a un valore <a href="#int"><strong>int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-564">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-565">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-565">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *LPINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-566"><span id="LPLONG"></span><span id="lplong"></span><strong>LPLONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-567">Puntatore a un oggetto <a href="#long"><strong>Long</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-567">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-568">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-568">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef long *LPLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-569"><span id="LPSTR"></span><span id="lpstr"></span><strong>LPSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-570">Puntatore a una stringa con terminazione null di caratteri di Windows a 8 bit (ANSI).</span><span class="sxs-lookup"><span data-stu-id="938f8-570">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="938f8-571">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-571">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-572">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-572">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *LPSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-573"><span id="LPTSTR"></span><span id="lptstr"></span><strong>LPTSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-574">Un <a href="#lpwstr"><strong>LPWSTR</strong></a> se è definito <strong>Unicode</strong> , un <a href="#lpstr"><strong>LPSTR</strong></a> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="938f8-574">An <a href="#lpwstr"><strong>LPWSTR</strong></a> if <strong>UNICODE</strong> is defined, an <a href="#lpstr"><strong>LPSTR</strong></a> otherwise.</span></span> <span data-ttu-id="938f8-575">Per ulteriori informazioni, vedere <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipi di dati di Windows per le stringhe</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-575">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="938f8-576">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-576">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-577">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-577">C++</span></span></th>
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
<td><span data-ttu-id="938f8-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-578"><span id="LPVOID"></span><span id="lpvoid"></span><strong>LPVOID</strong></span></span></td>
<td><p><span data-ttu-id="938f8-579">Puntatore a qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="938f8-579">A pointer to any type.</span></span></p>
<p><span data-ttu-id="938f8-580">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-580">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef void *LPVOID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-581"><span id="LPWORD"></span><span id="lpword"></span><strong>LPWORD</strong></span></span></td>
<td><p><span data-ttu-id="938f8-582">Puntatore a una <a href="#word"><strong>parola</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-582">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-583">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-583">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *LPWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-584"><span id="LPWSTR"></span><span id="lpwstr"></span><strong>LPWSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-585">Puntatore a una stringa con terminazione null di caratteri Unicode a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-585">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="938f8-586">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-586">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-587">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-587">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *LPWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-588"><span id="LRESULT"></span><span id="lresult"></span><strong>LRESULT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-589">Risultato firmato dell'elaborazione del messaggio.</span><span class="sxs-lookup"><span data-stu-id="938f8-589">Signed result of message processing.</span></span></p>
<p><span data-ttu-id="938f8-590">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-590">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef LONG_PTR LRESULT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-591"><span id="PBOOL"></span><span id="pbool"></span><strong>PBOOL</strong></span></span></td>
<td><p><span data-ttu-id="938f8-592">Puntatore a un <a href="#bool"><strong>bool</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-592">A pointer to a <a href="#bool"><strong>BOOL</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-593">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-593">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BOOL *PBOOL;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-594"><span id="PBOOLEAN"></span><span id="pboolean"></span><strong>PBOOLEAN</strong></span></span></td>
<td><p><span data-ttu-id="938f8-595">Puntatore a un <a href="#boolean"><strong>valore booleano</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-595">A pointer to a <a href="#boolean"><strong>BOOLEAN</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-596">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-596">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef BOOLEAN *PBOOLEAN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-597"><span id="PBYTE"></span><span id="pbyte"></span><strong>PBYTE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-598">Puntatore a un <a href="#byte"><strong>byte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-598">A pointer to a <a href="#byte"><strong>BYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-599">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-599">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef BYTE *PBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-600"><span id="PCHAR"></span><span id="pchar"></span><strong>PCHAR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-601">Puntatore a un oggetto <a href="#char"><strong>char</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-601">A pointer to a <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-602">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-602">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-603"><span id="PCSTR"></span><span id="pcstr"></span><strong>PCSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-604">Puntatore a una stringa costante con terminazione null di caratteri di Windows a 8 bit (ANSI).</span><span class="sxs-lookup"><span data-stu-id="938f8-604">A pointer to a constant null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="938f8-605">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-605">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-606">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-606">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST CHAR *PCSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-607"><span id="PCTSTR"></span><span id="pctstr"></span><strong>PCTSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-608"><a href="#pcwstr"><strong>PCWSTR</strong></a> se è definito <strong>Unicode</strong> , un <a href="#pcstr"><strong>PCSTR</strong></a> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="938f8-608">A <a href="#pcwstr"><strong>PCWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pcstr"><strong>PCSTR</strong></a> otherwise.</span></span> <span data-ttu-id="938f8-609">Per ulteriori informazioni, vedere <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipi di dati di Windows per le stringhe</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-609">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="938f8-610">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-610">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-611">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-611">C++</span></span></th>
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
<td><span data-ttu-id="938f8-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-612"><span id="PCWSTR"></span><span id="pcwstr"></span><strong>PCWSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-613">Puntatore a una stringa costante con terminazione null di caratteri Unicode a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-613">A pointer to a constant null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="938f8-614">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-614">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-615">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-615">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CONST WCHAR *PCWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-616"><span id="PDWORD"></span><span id="pdword"></span><strong>PDWORD</strong></span></span></td>
<td><p><span data-ttu-id="938f8-617">Puntatore a un <a href="#dword"><strong>valore DWORD</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-617">A pointer to a <a href="#dword"><strong>DWORD</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-618">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-618">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef DWORD *PDWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-619"><span id="PDWORDLONG"></span><span id="pdwordlong"></span><strong>PDWORDLONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-620">Puntatore a un <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-620">A pointer to a <a href="#dwordlong"><strong>DWORDLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-621">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-621">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef DWORDLONG *PDWORDLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-622"><span id="PDWORD_PTR"></span><span id="pdword_ptr"></span><strong>PDWORD_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-623">Puntatore a un <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-623">A pointer to a <a href="#dword_ptr"><strong>DWORD_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-624">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-624">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD_PTR *PDWORD_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-625"><span id="PDWORD32"></span><span id="pdword32"></span><strong>PDWORD32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-626">Puntatore a un <a href="#dword32"><strong>DWORD32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-626">A pointer to a <a href="#dword32"><strong>DWORD32</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-627">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-627">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD32 *PDWORD32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-628"><span id="PDWORD64"></span><span id="pdword64"></span><strong>PDWORD64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-629">Puntatore a un <a href="#dword64"><strong>DWORD64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-629">A pointer to a <a href="#dword64"><strong>DWORD64</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-630">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-630">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef DWORD64 *PDWORD64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-631"><span id="PFLOAT"></span><span id="pfloat"></span><strong>PFLOAT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-632">Puntatore a un valore <a href="#float"><strong>float</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-632">A pointer to a <a href="#float"><strong>FLOAT</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-633">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-633">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef FLOAT *PFLOAT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-634"><span id="PHALF_PTR"></span><span id="phalf_ptr"></span><strong>PHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-635">Puntatore a un <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-635">A pointer to a <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-636">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-636">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-637">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-637">C++</span></span></th>
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
<td><span data-ttu-id="938f8-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-638"><span id="PHANDLE"></span><span id="phandle"></span><strong>PHANDLE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-639">Puntatore a un <a href="#handle"><strong>handle</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-639">A pointer to a <a href="#handle"><strong>HANDLE</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-640">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-640">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef HANDLE *PHANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-641"><span id="PHKEY"></span><span id="phkey"></span><strong>PHKEY</strong></span></span></td>
<td><p><span data-ttu-id="938f8-642">Puntatore a un <a href="#hkey"><strong>HKEY</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-642">A pointer to an <a href="#hkey"><strong>HKEY</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-643">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-643">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef HKEY *PHKEY;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-644"><span id="PINT"></span><span id="pint"></span><strong>PINT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-644"><span id="PINT"></span><span id="pint"></span><strong>PINT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-645">Puntatore a un valore <a href="#int"><strong>int</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-645">A pointer to an <a href="#int"><strong>INT</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-646">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-646">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef int *PINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-647"><span id="PINT_PTR"></span><span id="pint_ptr"></span><strong>PINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-648">Puntatore a un <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-648">A pointer to an <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-649">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-649">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT_PTR *PINT_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-650"><span id="PINT8"></span><span id="pint8"></span><strong>PINT8</strong></span></span></td>
<td><p><span data-ttu-id="938f8-651">Puntatore a un <a href="#int8"><strong>int8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-651">A pointer to an <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-652">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-652">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT8 *PINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-653"><span id="PINT16"></span><span id="pint16"></span><strong>PINT16</strong></span></span></td>
<td><p><span data-ttu-id="938f8-654">Puntatore a un oggetto <a href="#int16"><strong>Int16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-654">A pointer to an <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-655">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-655">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT16 *PINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-656"><span id="PINT32"></span><span id="pint32"></span><strong>PINT32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-657">Puntatore a un <a href="#int32"><strong>Int32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-657">A pointer to an <a href="#int32"><strong>INT32</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-658">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-658">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT32 *PINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-659"><span id="PINT64"></span><span id="pint64"></span><strong>PINT64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-660">Puntatore a un <a href="#int64"><strong>Int64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-660">A pointer to an <a href="#int64"><strong>INT64</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-661">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-661">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef INT64 *PINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-662"><span id="PLCID"></span><span id="plcid"></span><strong>PLCID</strong></span></span></td>
<td><p><span data-ttu-id="938f8-663">Puntatore a un <a href="#lcid"><strong>LCID</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-663">A pointer to an <a href="#lcid"><strong>LCID</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-664">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-664">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef PDWORD PLCID;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-665"><span id="PLONG"></span><span id="plong"></span><strong>PLONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-666">Puntatore a un oggetto <a href="#long"><strong>Long</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-666">A pointer to a <a href="#long"><strong>LONG</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-667">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-667">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONG *PLONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-668"><span id="PLONGLONG"></span><span id="plonglong"></span><strong>PLONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-669">Puntatore a un <a href="#longlong"><strong>LONGLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-669">A pointer to a <a href="#longlong"><strong>LONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-670">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-670">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG *PLONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-671"><span id="PLONG_PTR"></span><span id="plong_ptr"></span><strong>PLONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-672">Puntatore a un <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-672">A pointer to a <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-673">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-673">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR *PLONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-674"><span id="PLONG32"></span><span id="plong32"></span><strong>PLONG32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-675">Puntatore a un <a href="#long32"><strong>LONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-675">A pointer to a <a href="#long32"><strong>LONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-676">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-676">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG32 *PLONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-677"><span id="PLONG64"></span><span id="plong64"></span><strong>PLONG64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-678">Puntatore a un <a href="#long64"><strong>long64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-678">A pointer to a <a href="#long64"><strong>LONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-679">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-679">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG64 *PLONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-680"><span id="POINTER_32"></span><span id="pointer_32"></span><strong>POINTER_32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-681">Puntatore a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-681">A 32-bit pointer.</span></span> <span data-ttu-id="938f8-682">In un sistema a 32 bit, si tratta di un puntatore nativo.</span><span class="sxs-lookup"><span data-stu-id="938f8-682">On a 32-bit system, this is a native pointer.</span></span> <span data-ttu-id="938f8-683">In un sistema a 64 bit, si tratta di un puntatore a 64 bit troncato.</span><span class="sxs-lookup"><span data-stu-id="938f8-683">On a 64-bit system, this is a truncated 64-bit pointer.</span></span></p>
<p><span data-ttu-id="938f8-684">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-684">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-685">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-685">C++</span></span></th>
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
<td><span data-ttu-id="938f8-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-686"><span id="POINTER_64"></span><span id="pointer_64"></span><strong>POINTER_64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-687">Puntatore a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-687">A 64-bit pointer.</span></span> <span data-ttu-id="938f8-688">In un sistema a 64 bit, si tratta di un puntatore nativo.</span><span class="sxs-lookup"><span data-stu-id="938f8-688">On a 64-bit system, this is a native pointer.</span></span> <span data-ttu-id="938f8-689">In un sistema a 32 bit, si tratta di un puntatore a 32 bit esteso con segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-689">On a 32-bit system, this is a sign-extended 32-bit pointer.</span></span></p>
<p><span data-ttu-id="938f8-690">Si noti che non è sicuro presupporre lo stato del bit del puntatore elevato.</span><span class="sxs-lookup"><span data-stu-id="938f8-690">Note that it is not safe to assume the state of the high pointer bit.</span></span></p>
<p><span data-ttu-id="938f8-691">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-691">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-692">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-692">C++</span></span></th>
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
<td><span data-ttu-id="938f8-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-693"><span id="POINTER_SIGNED"></span><span id="pointer_signed"></span><strong>POINTER_SIGNED</strong></span></span></td>
<td><p><span data-ttu-id="938f8-694">Puntatore con segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-694">A signed pointer.</span></span></p>
<p><span data-ttu-id="938f8-695">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-695">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_SIGNED __sptr</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-696"><span id="POINTER_UNSIGNED"></span><span id="pointer_unsigned"></span><strong>POINTER_UNSIGNED</strong></span></span></td>
<td><p><span data-ttu-id="938f8-697">Puntatore senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-697">An unsigned pointer.</span></span></p>
<p><span data-ttu-id="938f8-698">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-698">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>#define POINTER_UNSIGNED __uptr</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-699"><span id="PSHORT"></span><span id="pshort"></span><strong>PSHORT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-700">Puntatore a <a href="#short"><strong>short</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-700">A pointer to a <a href="#short"><strong>SHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-701">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-701">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef SHORT *PSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-702"><span id="PSIZE_T"></span><span id="psize_t"></span><strong>PSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="938f8-703">Puntatore a un <a href="#size_t"><strong>size_t</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-703">A pointer to a <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-704">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-704">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SIZE_T *PSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-705"><span id="PSSIZE_T"></span><span id="pssize_t"></span><strong>PSSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="938f8-706">Puntatore a un <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-706">A pointer to a <a href="#ssize_t"><strong>SSIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-707">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-707">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef SSIZE_T *PSSIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-708"><span id="PSTR"></span><span id="pstr"></span><strong>PSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-709">Puntatore a una stringa con terminazione null di caratteri di Windows a 8 bit (ANSI).</span><span class="sxs-lookup"><span data-stu-id="938f8-709">A pointer to a null-terminated string of 8-bit Windows (ANSI) characters.</span></span> <span data-ttu-id="938f8-710">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-710">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-711">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-711">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef CHAR *PSTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-712"><span id="PTBYTE"></span><span id="ptbyte"></span><strong>PTBYTE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-713">Puntatore a un <a href="#tbyte"><strong>Tbyte</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-713">A pointer to a <a href="#tbyte"><strong>TBYTE</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-714">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-714">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TBYTE *PTBYTE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-715"><span id="PTCHAR"></span><span id="ptchar"></span><strong>PTCHAR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-716">Puntatore a un <a href="#tchar"><strong>TCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-716">A pointer to a <a href="#tchar"><strong>TCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-717">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-717">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef TCHAR *PTCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-718"><span id="PTSTR"></span><span id="ptstr"></span><strong>PTSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-719"><a href="#pwstr"><strong>PWSTR</strong></a> se è definito <strong>Unicode</strong> , un <a href="#pstr"><strong>pstr</strong></a> in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="938f8-719">A <a href="#pwstr"><strong>PWSTR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#pstr"><strong>PSTR</strong></a> otherwise.</span></span> <span data-ttu-id="938f8-720">Per ulteriori informazioni, vedere <a href="/windows/desktop/Intl/windows-data-types-for-strings">tipi di dati di Windows per le stringhe</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-720">For more information, see <a href="/windows/desktop/Intl/windows-data-types-for-strings">Windows Data Types for Strings</a>.</span></span></p>
<p><span data-ttu-id="938f8-721">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-721">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-722">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-722">C++</span></span></th>
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
<td><span data-ttu-id="938f8-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-723"><span id="PUCHAR"></span><span id="puchar"></span><strong>PUCHAR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-724">Puntatore a un <a href="#uchar"><strong>UCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-724">A pointer to a <a href="#uchar"><strong>UCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-725">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-725">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UCHAR *PUCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-726"><span id="PUHALF_PTR"></span><span id="puhalf_ptr"></span><strong>PUHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-727">Puntatore a un <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-727">A pointer to a <a href="#uhalf_ptr"><strong>UHALF_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-728">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-728">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-729">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-729">C++</span></span></th>
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
<td><span data-ttu-id="938f8-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-730"><span id="PUINT"></span><span id="puint"></span><strong>PUINT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-731">Puntatore a <a href="#uint"><strong>uint</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-731">A pointer to a <a href="#uint"><strong>UINT</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-732">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-732">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT *PUINT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-733"><span id="PUINT_PTR"></span><span id="puint_ptr"></span><strong>PUINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-734">Puntatore a un <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-734">A pointer to a <a href="#uint_ptr"><strong>UINT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-735">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-735">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT_PTR *PUINT_PTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-736"><span id="PUINT8"></span><span id="puint8"></span><strong>PUINT8</strong></span></span></td>
<td><p><span data-ttu-id="938f8-737">Puntatore a un <a href="#uint8"><strong>Uint8</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-737">A pointer to a <a href="#uint8"><strong>UINT8</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-738">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-738">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT8 *PUINT8;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-739"><span id="PUINT16"></span><span id="puint16"></span><strong>PUINT16</strong></span></span></td>
<td><p><span data-ttu-id="938f8-740">Puntatore a un oggetto <a href="#uint16"><strong>UInt16</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-740">A pointer to a <a href="#uint16"><strong>UINT16</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-741">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-741">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT16 *PUINT16;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-742"><span id="PUINT32"></span><span id="puint32"></span><strong>PUINT32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-743">Puntatore a un oggetto <a href="#uint32"><strong>UInt32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-743">A pointer to a <a href="#uint32"><strong>UINT32</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-744">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-744">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT32 *PUINT32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-745"><span id="PUINT64"></span><span id="puint64"></span><strong>PUINT64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-746">Puntatore a <a href="#uint64"><strong>UInt64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-746">A pointer to a <a href="#uint64"><strong>UINT64</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-747">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-747">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef UINT64 *PUINT64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-748"><span id="PULONG"></span><span id="pulong"></span><strong>PULONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-749">Puntatore a un <a href="#ulong"><strong>ULONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-749">A pointer to a <a href="#ulong"><strong>ULONG</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-750">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-750">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONG *PULONG;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-751"><span id="PULONGLONG"></span><span id="pulonglong"></span><strong>PULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-752">Puntatore a un <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-752">A pointer to a <a href="#ulonglong"><strong>ULONGLONG</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-753">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-753">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef ULONGLONG *PULONGLONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-754"><span id="PULONG_PTR"></span><span id="pulong_ptr"></span><strong>PULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-755">Puntatore a un <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-755">A pointer to a <a href="#ulong_ptr"><strong>ULONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-756">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-756">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR *PULONG_PTR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-757"><span id="PULONG32"></span><span id="pulong32"></span><strong>PULONG32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-758">Puntatore a un <a href="#ulong32"><strong>ULONG32</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-758">A pointer to a <a href="#ulong32"><strong>ULONG32</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-759">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-759">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG32 *PULONG32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-760"><span id="PULONG64"></span><span id="pulong64"></span><strong>PULONG64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-761">Puntatore a un <a href="#ulong64"><strong>ULONG64</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-761">A pointer to a <a href="#ulong64"><strong>ULONG64</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-762">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-762">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG64 *PULONG64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-763"><span id="PUSHORT"></span><span id="pushort"></span><strong>PUSHORT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-764">Puntatore a un <a href="#ushort"><strong>ushort</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-764">A pointer to a <a href="#ushort"><strong>USHORT</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-765">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-765">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef USHORT *PUSHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-766"><span id="PVOID"></span><span id="pvoid"></span><strong>PVOID</strong></span></span></td>
<td><p><span data-ttu-id="938f8-767">Puntatore a qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="938f8-767">A pointer to any type.</span></span></p>
<p><span data-ttu-id="938f8-768">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-768">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef void *PVOID;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-769"><span id="PWCHAR"></span><span id="pwchar"></span><strong>PWCHAR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-770">Puntatore a un <a href="#wchar"><strong>WCHAR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-770">A pointer to a <a href="#wchar"><strong>WCHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-771">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-771">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-772"><span id="PWORD"></span><span id="pword"></span><strong>PWORD</strong></span></span></td>
<td><p><span data-ttu-id="938f8-773">Puntatore a una <a href="#word"><strong>parola</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-773">A pointer to a <a href="#word"><strong>WORD</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-774">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-774">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef WORD *PWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-775"><span id="PWSTR"></span><span id="pwstr"></span><strong>PWSTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-776">Puntatore a una stringa con terminazione null di caratteri Unicode a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-776">A pointer to a null-terminated string of 16-bit Unicode characters.</span></span> <span data-ttu-id="938f8-777">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-777">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-778">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-778">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef WCHAR *PWSTR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-779"><span id="QWORD"></span><span id="qword"></span><strong>QWORD</strong></span></span></td>
<td><p><span data-ttu-id="938f8-780">Intero senza segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-780">A 64-bit unsigned integer.</span></span></p>
<p><span data-ttu-id="938f8-781">Questo tipo viene dichiarato nel modo seguente:</span><span class="sxs-lookup"><span data-stu-id="938f8-781">This type is declared as follows:</span></span></p>
<p><code>typedef unsigned __int64 QWORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-782"><span id="SC_HANDLE"></span><span id="sc_handle"></span><strong>SC_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-783">Handle per un database di gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="938f8-783">A handle to a service control manager database.</span></span> <span data-ttu-id="938f8-784">Per ulteriori informazioni, vedere <a href="/windows/desktop/Services/scm-handles">handle SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-784">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="938f8-785">Questo tipo viene dichiarato in WinSvc. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-785">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SC_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-786"><span id="SC_LOCK"></span><span id="sc_lock"></span><strong>SC_LOCK</strong></span></span></td>
<td><p><span data-ttu-id="938f8-787">Un blocco a un database di gestione controllo servizi.</span><span class="sxs-lookup"><span data-stu-id="938f8-787">A lock to a service control manager database.</span></span> <span data-ttu-id="938f8-788">Per ulteriori informazioni, vedere <a href="/windows/desktop/Services/scm-handles">handle SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-788">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="938f8-789">Questo tipo viene dichiarato in WinSvc. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-789">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef LPVOID SC_LOCK;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-790"><span id="SERVICE_STATUS_HANDLE"></span><span id="service_status_handle"></span><strong>SERVICE_STATUS_HANDLE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-791">Handle per un valore di stato del servizio.</span><span class="sxs-lookup"><span data-stu-id="938f8-791">A handle to a service status value.</span></span> <span data-ttu-id="938f8-792">Per ulteriori informazioni, vedere <a href="/windows/desktop/Services/scm-handles">handle SCM</a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-792">For more information, see <a href="/windows/desktop/Services/scm-handles">SCM Handles</a>.</span></span></p>
<p><span data-ttu-id="938f8-793">Questo tipo viene dichiarato in WinSvc. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-793">This type is declared in WinSvc.h as follows:</span></span></p>
<p><code>typedef HANDLE SERVICE_STATUS_HANDLE;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-794"><span id="SHORT"></span><span id="short"></span><strong>BREVE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-794"><span id="SHORT"></span><span id="short"></span><strong>SHORT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-795">Intero A 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-795">A 16-bit integer.</span></span> <span data-ttu-id="938f8-796">L'intervallo è compreso tra-32768 e 32767 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-796">The range is -32768 through 32767 decimal.</span></span></p>
<p><span data-ttu-id="938f8-797">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-797">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef short SHORT;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-798"><span id="SIZE_T"></span><span id="size_t"></span><strong>SIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="938f8-799">Numero massimo di byte a cui può puntare un puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-799">The maximum number of bytes to which a pointer can point.</span></span> <span data-ttu-id="938f8-800">Utilizzare per un conteggio che deve estendersi all'intervallo completo di un puntatore.</span><span class="sxs-lookup"><span data-stu-id="938f8-800">Use for a count that must span the full range of a pointer.</span></span></p>
<p><span data-ttu-id="938f8-801">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-801">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef ULONG_PTR SIZE_T;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-802"><span id="SSIZE_T"></span><span id="ssize_t"></span><strong>SSIZE_T</strong></span></span></td>
<td><p><span data-ttu-id="938f8-803">Versione con segno di <a href="#size_t"><strong>size_t</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="938f8-803">A signed version of <a href="#size_t"><strong>SIZE_T</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-804">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-804">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef LONG_PTR SSIZE_T;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-805"><span id="TBYTE"></span><span id="tbyte"></span><strong>TBYTE</strong></span></span></td>
<td><p><span data-ttu-id="938f8-806">Oggetto <a href="#wchar"><strong>WCHAR</strong></a> se è definito <strong>Unicode</strong> , in caso contrario <a href="#char"><strong>char</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="938f8-806">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="938f8-807">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-807">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-808">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-808">C++</span></span></th>
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
<td><span data-ttu-id="938f8-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-809"><span id="TCHAR"></span><span id="tchar"></span><strong>TCHAR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-810">Oggetto <a href="#wchar"><strong>WCHAR</strong></a> se è definito <strong>Unicode</strong> , in caso contrario <a href="#char"><strong>char</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="938f8-810">A <a href="#wchar"><strong>WCHAR</strong></a> if <strong>UNICODE</strong> is defined, a <a href="#char"><strong>CHAR</strong></a> otherwise.</span></span></p>
<p><span data-ttu-id="938f8-811">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-811">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-812">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-812">C++</span></span></th>
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
<td><span data-ttu-id="938f8-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-813"><span id="UCHAR"></span><span id="uchar"></span><strong>UCHAR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-814">Un <a href="#char"><strong>carattere</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-814">An unsigned <a href="#char"><strong>CHAR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-815">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-815">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned char UCHAR;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-816"><span id="UHALF_PTR"></span><span id="uhalf_ptr"></span><strong>UHALF_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-817"><a href="#half_ptr"><strong>HALF_PTR</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-817">An unsigned <a href="#half_ptr"><strong>HALF_PTR</strong></a>.</span></span> <span data-ttu-id="938f8-818">Utilizzare all'interno di una struttura che contiene un puntatore e due campi di piccole dimensioni.</span><span class="sxs-lookup"><span data-stu-id="938f8-818">Use within a structure that contains a pointer and two small fields.</span></span></p>
<p><span data-ttu-id="938f8-819">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-819">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-820">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-820">C++</span></span></th>
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
<td><span data-ttu-id="938f8-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-821"><span id="UINT"></span><span id="uint"></span><strong>UINT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-822"><a href="#int"><strong>Int</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-822">An unsigned <a href="#int"><strong>INT</strong></a>.</span></span> <span data-ttu-id="938f8-823">L'intervallo è compreso tra 0 e 4294967295 decimale.</span><span class="sxs-lookup"><span data-stu-id="938f8-823">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="938f8-824">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-824">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-825"><span id="UINT_PTR"></span><span id="uint_ptr"></span><strong>UINT_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-826"><a href="#int_ptr"><strong>INT_PTR</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-826">An unsigned <a href="#int_ptr"><strong>INT_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-827">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-827">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-828">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-828">C++</span></span></th>
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
<td><span data-ttu-id="938f8-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-829"><span id="UINT8"></span><span id="uint8"></span><strong>UINT8</strong></span></span></td>
<td><p><span data-ttu-id="938f8-830"><a href="#int8"><strong>Int8</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-830">An unsigned <a href="#int8"><strong>INT8</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-831">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-831">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  char UINT8;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-832"><span id="UINT16"></span><span id="uint16"></span><strong>UINT16</strong></span></span></td>
<td><p><span data-ttu-id="938f8-833">Un oggetto <a href="#int16"><strong>Int16</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-833">An unsigned <a href="#int16"><strong>INT16</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-834">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-834">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned  short UINT16;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-835"><span id="UINT32"></span><span id="uint32"></span><strong>UINT32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-836"><a href="#int32"><strong>Int32</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-836">An unsigned <a href="#int32"><strong>INT32</strong></a>.</span></span> <span data-ttu-id="938f8-837">L'intervallo è compreso tra 0 e 4294967295 decimale.</span><span class="sxs-lookup"><span data-stu-id="938f8-837">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="938f8-838">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-838">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int UINT32;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-839"><span id="UINT64"></span><span id="uint64"></span><strong>UINT64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-840"><a href="#int64"><strong>Int64</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-840">An unsigned <a href="#int64"><strong>INT64</strong></a>.</span></span> <span data-ttu-id="938f8-841">L'intervallo è compreso tra 0 e 18.446.744.073.709.551.615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-841">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="938f8-842">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-842">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef usigned __int 64 UINT64;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-843"><span id="ULONG"></span><span id="ulong"></span><strong>ULONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-844"><a href="#long"><strong>Long</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-844">An unsigned <a href="#long"><strong>LONG</strong></a>.</span></span> <span data-ttu-id="938f8-845">L'intervallo è compreso tra 0 e 4294967295 decimale.</span><span class="sxs-lookup"><span data-stu-id="938f8-845">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="938f8-846">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-846">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned long ULONG;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-847"><span id="ULONGLONG"></span><span id="ulonglong"></span><strong>ULONGLONG</strong></span></span></td>
<td><p><span data-ttu-id="938f8-848">Intero senza segno a 64 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-848">A 64-bit unsigned integer.</span></span> <span data-ttu-id="938f8-849">L'intervallo è compreso tra 0 e 18.446.744.073.709.551.615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-849">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="938f8-850">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-850">This type is declared in WinNT.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-851">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-851">C++</span></span></th>
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
<td><span data-ttu-id="938f8-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-852"><span id="ULONG_PTR"></span><span id="ulong_ptr"></span><strong>ULONG_PTR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-853"><a href="#long_ptr"><strong>LONG_PTR</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-853">An unsigned <a href="#long_ptr"><strong>LONG_PTR</strong></a>.</span></span></p>
<p><span data-ttu-id="938f8-854">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-854">This type is declared in BaseTsd.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-855">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-855">C++</span></span></th>
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
<td><span data-ttu-id="938f8-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-856"><span id="ULONG32"></span><span id="ulong32"></span><strong>ULONG32</strong></span></span></td>
<td><p><span data-ttu-id="938f8-857"><a href="#long32"><strong>LONG32</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-857">An unsigned <a href="#long32"><strong>LONG32</strong></a>.</span></span> <span data-ttu-id="938f8-858">L'intervallo è compreso tra 0 e 4294967295 decimale.</span><span class="sxs-lookup"><span data-stu-id="938f8-858">The range is 0 through 4294967295 decimal.</span></span></p>
<p><span data-ttu-id="938f8-859">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-859">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned int ULONG32;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-860"><span id="ULONG64"></span><span id="ulong64"></span><strong>ULONG64</strong></span></span></td>
<td><p><span data-ttu-id="938f8-861"><a href="#long64"><strong>Long64</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-861">An unsigned <a href="#long64"><strong>LONG64</strong></a>.</span></span> <span data-ttu-id="938f8-862">L'intervallo è compreso tra 0 e 18.446.744.073.709.551.615 Decimal.</span><span class="sxs-lookup"><span data-stu-id="938f8-862">The range is 0 through 18446744073709551615 decimal.</span></span></p>
<p><span data-ttu-id="938f8-863">Questo tipo viene dichiarato in BaseTsd. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-863">This type is declared in BaseTsd.h as follows:</span></span></p>
<p><code>typedef unsigned __int64 ULONG64;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-864"><span id="UNICODE_STRING"></span><span id="unicode_string"></span><strong>UNICODE_STRING</strong></span></span></td>
<td><p><span data-ttu-id="938f8-865">Stringa Unicode.</span><span class="sxs-lookup"><span data-stu-id="938f8-865">A Unicode string.</span></span></p>
<p><span data-ttu-id="938f8-866">Questo tipo viene dichiarato in Winternl. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-866">This type is declared in Winternl.h as follows:</span></span></p>
<div class="code">
<span data-codelanguage="ManagedCPlusPlus"></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="938f8-867">C++</span><span class="sxs-lookup"><span data-stu-id="938f8-867">C++</span></span></th>
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
<td><span data-ttu-id="938f8-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-868"><span id="USHORT"></span><span id="ushort"></span><strong>USHORT</strong></span></span></td>
<td><p><span data-ttu-id="938f8-869"><a href="#short"><strong>Short</strong></a>senza segno.</span><span class="sxs-lookup"><span data-stu-id="938f8-869">An unsigned <a href="#short"><strong>SHORT</strong></a>.</span></span> <span data-ttu-id="938f8-870">L'intervallo è compreso tra 0 e 65535 decimale.</span><span class="sxs-lookup"><span data-stu-id="938f8-870">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="938f8-871">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-871">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short USHORT;</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-872"><span id="USN"></span><span id="usn"></span><strong>USN</strong></span></span></td>
<td><p><span data-ttu-id="938f8-873">Numero di sequenza di aggiornamento (USN).</span><span class="sxs-lookup"><span data-stu-id="938f8-873">An update sequence number (USN).</span></span></p>
<p><span data-ttu-id="938f8-874">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-874">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef LONGLONG USN;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-875"><span id="VOID"></span><span id="void"></span><strong>VUOTO</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-875"><span id="VOID"></span><span id="void"></span><strong>VOID</strong></span></span></td>
<td><p><span data-ttu-id="938f8-876">Qualsiasi tipo.</span><span class="sxs-lookup"><span data-stu-id="938f8-876">Any type.</span></span></p>
<p><span data-ttu-id="938f8-877">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-877">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>#define VOID void</code></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-878"><span id="WCHAR"></span><span id="wchar"></span><strong>WCHAR</strong></span></span></td>
<td><p><span data-ttu-id="938f8-879">Carattere Unicode A 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-879">A 16-bit Unicode character.</span></span> <span data-ttu-id="938f8-880">Per altre informazioni, vedere <a href="/windows/desktop/gdi/character-sets-used-by-fonts">set di caratteri usati dai tipi di</a>carattere.</span><span class="sxs-lookup"><span data-stu-id="938f8-880">For more information, see <a href="/windows/desktop/gdi/character-sets-used-by-fonts">Character Sets Used By Fonts</a>.</span></span></p>
<p><span data-ttu-id="938f8-881">Questo tipo è dichiarato in WinNT. h come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="938f8-881">This type is declared in WinNT.h as follows:</span></span></p>
<p><code>typedef wchar_t WCHAR;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-882"><span id="WINAPI"></span><span id="winapi"></span><strong>WINAPI</strong></span></span></td>
<td><p><span data-ttu-id="938f8-883">Convenzione di chiamata per le funzioni di sistema.</span><span class="sxs-lookup"><span data-stu-id="938f8-883">The calling convention for system functions.</span></span></p>
<p><span data-ttu-id="938f8-884">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-884">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>#define WINAPI __stdcall</code></p>
<p><span data-ttu-id="938f8-885"><strong>Callback</strong>, <strong>WINAPI</strong>e <strong>APIENTRY</strong> vengono utilizzati tutti per definire funzioni con la convenzione di chiamata __stdcall.</span><span class="sxs-lookup"><span data-stu-id="938f8-885"><strong>CALLBACK</strong>, <strong>WINAPI</strong>, and <strong>APIENTRY</strong> are all used to define functions with the __stdcall calling convention.</span></span> <span data-ttu-id="938f8-886">La maggior parte delle funzioni nell'API Windows viene dichiarata usando <strong>WINAPI</strong>.</span><span class="sxs-lookup"><span data-stu-id="938f8-886">Most functions in the Windows API are declared using <strong>WINAPI</strong>.</span></span> <span data-ttu-id="938f8-887">È possibile utilizzare <strong>callback</strong> per le funzioni di callback implementate per identificare la funzione come funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="938f8-887">You may wish to use <strong>CALLBACK</strong> for the callback functions that you implement to help identify the function as a callback function.</span></span></p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="938f8-888"><span id="WORD"></span><span id="word"></span><strong>WORD</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-888"><span id="WORD"></span><span id="word"></span><strong>WORD</strong></span></span></td>
<td><p><span data-ttu-id="938f8-889">Numero intero non firmato a 16 bit.</span><span class="sxs-lookup"><span data-stu-id="938f8-889">A 16-bit unsigned integer.</span></span> <span data-ttu-id="938f8-890">L'intervallo è compreso tra 0 e 65535 decimale.</span><span class="sxs-lookup"><span data-stu-id="938f8-890">The range is 0 through 65535 decimal.</span></span></p>
<p><span data-ttu-id="938f8-891">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-891">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef unsigned short WORD;</code></p></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="938f8-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span><span class="sxs-lookup"><span data-stu-id="938f8-892"><span id="WPARAM"></span><span id="wparam"></span><strong>WPARAM</strong></span></span></td>
<td><p><span data-ttu-id="938f8-893">Parametro del messaggio.</span><span class="sxs-lookup"><span data-stu-id="938f8-893">A message parameter.</span></span></p>
<p><span data-ttu-id="938f8-894">Questo tipo viene dichiarato in WinDef. h come segue:</span><span class="sxs-lookup"><span data-stu-id="938f8-894">This type is declared in WinDef.h as follows:</span></span></p>
<p><code>typedef UINT_PTR WPARAM;</code></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="938f8-895">Requisiti</span><span class="sxs-lookup"><span data-stu-id="938f8-895">Requirements</span></span>



| <span data-ttu-id="938f8-896">Requisito</span><span class="sxs-lookup"><span data-stu-id="938f8-896">Requirement</span></span> | <span data-ttu-id="938f8-897">Valore</span><span class="sxs-lookup"><span data-stu-id="938f8-897">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="938f8-898">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="938f8-898">Minimum supported client</span></span><br/> | <span data-ttu-id="938f8-899">\[Solo app desktop Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="938f8-899">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                         |
| <span data-ttu-id="938f8-900">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="938f8-900">Minimum supported server</span></span><br/> | <span data-ttu-id="938f8-901">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="938f8-901">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                |
| <span data-ttu-id="938f8-902">Intestazione</span><span class="sxs-lookup"><span data-stu-id="938f8-902">Header</span></span><br/>                   | <dl> <span data-ttu-id="938f8-903"><dt>BaseTsd. h; </dt> <dt>WinDef. h; </dt> <dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="938f8-903"><dt>BaseTsd.h; </dt> <dt>WinDef.h; </dt> <dt>WinNT.h</dt></span></span> </dl> |
