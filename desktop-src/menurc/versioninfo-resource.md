---
title: Risorsa VERSIONINFO
description: Definisce una risorsa di informazioni sulla versione. La risorsa contiene tali informazioni sul file come numero di versione, sistema operativo previsto e nome file originale. La risorsa deve essere usata con le funzioni di informazioni sulla versione.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menu delle risorse VERSIONINFO e altre risorse
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d6708b4fefc564685a9989140e5f07dd20714e8bbcb60c53710f43cbfee4aa7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118971870"
---
# <a name="versioninfo-resource"></a>Risorsa VERSIONINFO

Definisce una risorsa di informazioni sulla versione. La risorsa contiene tali informazioni sul file come numero di versione, sistema operativo previsto e nome file originale. La risorsa deve essere usata con le funzioni [di informazioni sulla](./version-information.md) versione.

Esistono due modi per formattare **un'istruzione VERSIONINFO:**

``` syntax
versionID VERSIONINFO fixed-info  { block-statement . . . }
```

\- - oppure -

``` syntax
versionID VERSIONINFO 
fixed-info
BEGIN
block-statement
. . .
END
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*Versionid*
</dt> <dd>

Identificatore della risorsa di informazioni sulla versione. Questo valore deve essere 1.

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*fixed-info*
</dt> <dd>

Informazioni sulla versione, ad esempio la versione del file e il sistema operativo previsto. Questo parametro è costituito dalle istruzioni seguenti.



| Istruzione                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Versione FILEVERSION**          | Numero di versione binario del file. La *versione* è costituita da due interi a 32 bit, definiti da quattro interi a 16 bit. Ad esempio, "FILEVERSION 3,10,0,61" viene convertito in due due parole: 0x0003000a e 0x0000003d, in questo ordine. Pertanto, se *la* versione è definita dai valori **DWORD** *dw1* e *dw2*, devono essere visualizzati nell'istruzione **FILEVERSION** come segue: `HIWORD(dw1)` , , , `LOWORD(dw1)` `HIWORD(dw2)` `LOWORD(dw2)` . |
| **Versione PRODUCTVERSION**       | Numero di versione binario del prodotto con cui viene distribuito il file. Il *parametro* version è due interi a 32 bit, definiti da quattro interi a 16 bit. Per altre informazioni sulla *versione*, vedere la **descrizione di FILEVERSION.**                                                                                                                                                                                                           |
| **FILEFLAGSMASK** *fileflagsmask* | Indica quali bit **dell'istruzione FILEFLAGS** sono validi. Per le applicazioni a 16 bit Windows, questo valore è 0x3f.                                                                                                                                                                                                                                                                                                                                          |
| **FileFLAGS** *fileflags*         | Attributi del file.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **FILEOS** *fileos*               | Sistema operativo per cui è stato progettato questo file. Il *parametro fileos* può essere uno dei valori del sistema operativo specificati nella sezione Osservazioni.                                                                                                                                                                                                                                                                                               |
| **Tipo di** file *FILETYPE*           | Tipo generale di file. Il *parametro filetype* può essere uno dei valori del tipo di file elencati nella sezione Osservazioni.                                                                                                                                                                                                                                                                                                                                |
| **Sottotipo FILESUBTYPE**          | Funzione del file. Il *parametro del sottotipo* è zero, a meno che il *parametro filetype* nell'istruzione **FILETYPE** non sia VFT \_ DRV, VFT \_ FONT o VFT \_ VXD. Per un elenco dei valori dei sottotipi di file, vedere la sezione Osservazioni.                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*block-statement*
</dt> <dd>

Specifica uno o più blocchi di informazioni sulla versione. Un blocco può contenere informazioni di tipo stringa o informazioni sulle variabili. Per altre informazioni, vedere [**Blocco StringFileInfo o**](stringfileinfo-block.md) [**Blocco VarFileInfo.**](varfileinfo-block.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare le costanti specificate con l'istruzione **VERSIONINFO,** è necessario includere il file di intestazione Winver.h o Windows.h nel file di definizione delle risorse.

Nell'elenco seguente vengono descritti i parametri utilizzati **nell'istruzione VERSIONINFO:**

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*fileflags*
</dt> <dd>

Combinazione dei valori seguenti.



| Valore                      | Descrizione                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **VS \_ FF \_ DEBUG**          | Il file contiene informazioni di debug o viene compilato con le funzionalità di debug abilitate.                                                                                                                                                                                         |
| **PATCH DI VISUAL \_ STUDIO FF \_**        | Il file è stato modificato e non è identico al file di spedizione originale con lo stesso numero di versione.                                                                                                                                                                       |
| **VERSIONE PRELIMINARE DI VS \_ FF \_**     | Il file è una versione di sviluppo, non un prodotto rilasciato in commercio.                                                                                                                                                                                                         |
| **VS \_ FF \_ PRIVATEBUILD**   | Il file non è stato compilato usando le procedure di rilascio standard. Se questo valore viene specificato, il [**blocco StringFileInfo**](stringfileinfo-block.md) deve contenere una **stringa PrivateBuild.**                                                                                              |
| **VS \_ FF \_ SPECIALBUILD**   | Il file è stato compilato dalla società originale usando le procedure di rilascio standard, ma è una variante del file standard con lo stesso numero di versione. Se viene specificato questo valore, il [ **blocco di blocco StringFileInfo**](stringfileinfo-block.md) deve contenere una **stringa SpecialBuild.** |
| **VS \_ FFI \_ FILEFLAGSMASK** | Combinazione di tutti i valori precedenti.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*fileos*
</dt> <dd>

Uno dei valori seguenti.



| Valore                   | Descrizione                                                      |
|-------------------------|------------------------------------------------------------------|
| **VOS \_ UNKNOWN**        | Il sistema operativo per cui è stato progettato il file è sconosciuto. |
| **VOS \_ DOS**            | Il file è stato progettato per MS-DOS.                                    |
| **VOS \_ NT**             | Il file è stato progettato per le applicazioni a 32 bit Windows.                            |
| **VOS \_ \_ WINDOWS16**    | Il file è stato progettato per l'Windows a 16 bit.                            |
| **VOS \_ \_ WINDOWS32**    | Il file è stato progettato per le applicazioni a 32 bit Windows.                            |
| **VOS \_ DOS \_ WINDOWS16** | Il file è stato progettato per l'esecuzione Windows a 16 bit con MS-DOS.        |
| **VOS \_ DOS \_ WINDOWS32** | Il file è stato progettato per l'esecuzione Windows a 32 bit con MS-DOS.        |
| **VOS \_ NT \_ WINDOWS32**  | Il file è stato progettato per le applicazioni a 32 bit Windows.                            |



 

I valori 0x00002L, 0x00003L, 0x20000L e 0x30000L sono riservati.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*Filetype*
</dt> <dd>

Uno dei valori seguenti.



| Valore                | Descrizione                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ UNKNOWN**     | Il tipo di file è sconosciuto.                                                                                                       |
| **VFT \_ APP**         | Il file contiene un'applicazione.                                                                                               |
| **VFT \_ DLL**         | Il file contiene una libreria a collegamento dinamico (DLL).                                                                                 |
| **VFT \_ DRV**         | Il file contiene un driver di dispositivo. Se *filetype* è **VFT \_ DRV,** *il sottotipo* contiene una descrizione più specifica del driver. |
| **TIPO DI CARATTERE \_ VFT**        | Il file contiene un tipo di carattere. Se *filetype è* VFT \_ FONT, *subtype* contiene una descrizione più specifica del tipo di carattere.               |
| **VFT \_ VXD**         | Il file contiene un dispositivo virtuale.                                                                                             |
| **LIBRERIA \_ STATICA VFT \_** | Il file contiene una libreria a collegamento statico.                                                                                        |



 

Tutti gli altri valori sono riservati per l'uso da parte di Microsoft.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*Sottotipo*
</dt> <dd>

Informazioni aggiuntive sul tipo di file.

Se *filetype* specifica **VFT \_ DRV,** questo parametro può essere uno dei valori seguenti.



| Valore                             | Descrizione                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ UNKNOWN**                 | Il tipo di driver è sconosciuto.                   |
| **VFT2 \_ DRV \_ COMM**               | Il file contiene un driver per le comunicazioni.    |
| **STAMPANTE VFT2 \_ DRV \_**            | Il file contiene un driver della stampante.           |
| **TASTIERA VFT2 \_ \_ DRV**           | Il file contiene un driver della tastiera.          |
| **LINGUAGGIO \_ DRV VFT2 \_**           | Il file contiene un driver di linguaggio.          |
| **VFT2 \_ DRV \_ DISPLAY**            | Il file contiene un driver di visualizzazione.           |
| **VFT2 \_ DRV \_ MOUSE**              | Il file contiene un driver del mouse.             |
| **RETE \_ VFT2 DRV \_**            | Il file contiene un driver di rete.           |
| **SISTEMA \_ VFT2 DRV \_**             | Il file contiene un driver di sistema.            |
| **VFT2 \_ DRV \_ INSTALLABLE**        | Il file contiene un driver installabile.      |
| **AUDIO \_ VFT2 DRV \_**              | Il file contiene un driver audio.             |
| **VFT2 \_ DRV \_ VERSIONED \_ PRINTER** | Il file contiene un driver della stampante con versione. |



 

Se *filetype* specifica **VFT \_ FONT,** questo parametro può essere uno dei valori seguenti.



| Valore                    | Descrizione                    |
|--------------------------|--------------------------------|
| **VFT2 \_ UNKNOWN**        | Tipo di carattere sconosciuto.          |
| **VFT2 \_ FONT \_ RASTER**   | Il file contiene un tipo di carattere raster.   |
| **VETTORE CARATTERE VFT2 \_ \_**   | Il file contiene un tipo di carattere vettoriale.   |
| **VFT2 \_ FONT \_ TRUETYPE** | Il file contiene un tipo di carattere TrueType. |



 

Se *filetype* specifica VFT VXD, questo parametro deve essere l'identificatore del dispositivo virtuale \_ incluso nel blocco di controllo del dispositivo virtuale.

Tutti *i valori di sottotipo* non elencati qui sono riservati per l'uso da parte di Microsoft.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Uno dei codici lingua seguenti.



| Codice   | Linguaggio            | Codice   | Linguaggio                  |
|--------|---------------------|--------|---------------------------|
| 0x0401 | Arabo              | 0x0415 | Polacco                    |
| 0x0402 | Bulgaro           | 0x0416 | Portoghese (Brasile)       |
| 0x0403 | Catalano             | 0x0417 | Rhaeto-Romanic            |
| 0x0404 | Cinese tradizionale | 0x0418 | Romeno                  |
| 0x0405 | Ceco               | 0x0419 | Russo                   |
| 0x0406 | Danese              | 0x041A | Croato-Serbian (alfabeto latino)    |
| 0x0407 | Tedesco              | 0x041B | Slovacco                    |
| 0x0408 | Greco               | 0x041C | Albanese                  |
| 0x0409 | Inglese (Stati Uniti)        | 0x041D | Svedese                   |
| 0x040A | Castiliano spagnolo   | 0x041E | Thai                      |
| 0x040B | Finlandese             | 0x041F | Turco                   |
| 0x040C | Francese              | 0x0420 | Urdu                      |
| 0x040D | Ebraico              | 0x0421 | Bahasa                    |
| 0x040E | Ungherese           | 0x0804 | Cinese semplificato        |
| 0x040F | Islandese           | 0x0807 | Tedesco tedesco              |
| 0x0410 | Italiano             | 0x0809 | Regno unito. Inglese              |
| 0x0411 | Giapponese            | 0x080A | Spagnolo (Messico)          |
| 0x0412 | Coreano              | 0x080C | Francese francese francese            |
| 0x0413 | Olandese               | 0x0C0C | Francese (Canada)           |
| 0x0414 | Norvegese? Bokmal  | 0x100C | Francese svizzero              |
| 0x0810 | Italiano (Svizzera)       | 0x0816 | Portoghese (Portogallo)     |
| 0x0813 | Olandese (Olandese)       | 0x081A | Serbo-Croatian (alfabeto cirillico) |
| 0x0814 | Norvegese? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Uno degli identificatori di set di caratteri seguenti.



| Decimal | Valore esadecimale | Set di caratteri              |
|---------|-------------|----------------------------|
| 0       | 0000        | ASCII a 7 bit                |
| 932     | 03A4        | Giappone (MAIUSC ? JIS X-0208) |
| 949     | 03B5        | Corea del Sud (MAIUSC ? KSC 5601)   |
| 950     | 03B6        | Taiwan (Big5)              |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | Latin-2 (Europa orientale) |
| 1251    | 04E3        | Cirillico                   |
| 1252    | 04E4        | Multilingue               |
| 1253    | 04E5        | Greco                      |
| 1254    | 04E6        | Turco                    |
| 1255    | 04E7        | Ebraico                     |
| 1256    | 04E8        | Arabo                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*string-name*
</dt> <dd>

Uno dei nomi predefiniti seguenti.



| Nome                 | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Commenti**         | Informazioni aggiuntive che devono essere visualizzate a scopo diagnostico.                                                                                                                                                                                                                                    |
| **CompanyName**      | Società che ha prodotto il file, ad esempio "Microsoft Corporation" o "Standard Microsystems Corporation, Inc." Questa stringa è obbligatoria.                                                                                                                                                                   |
| **FileDescription**  | Descrizione del file da presentare agli utenti. Questa stringa può essere visualizzata in una casella di riepilogo quando l'utente sceglie i file da installare, ad esempio "Driver tastiera per AT-Style tastiera". Questa stringa è obbligatoria.                                                                                            |
| **FileVersion**      | Numero di versione del file, ad esempio "3.10" o "5.00.RC2". Questa stringa è obbligatoria.                                                                                                                                                                                                                      |
| **InternalName**     | Nome interno del file, se presente? Ad esempio, un nome di modulo se il file è una libreria a collegamento dinamico. Se il file non ha un nome interno, questa stringa deve essere il nome file originale, senza estensione. Questa stringa è obbligatoria.                                                                       |
| **LegalCopyright**   | Informazioni sul copyright che si applicano al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, le date di copyright e così via. Questa stringa è facoltativa.                                                                                                                                             |
| **LegalTrademarks**  | Marchi e marchi registrati applicabili al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, i numeri dei marchi e così via. Questa stringa è facoltativa.                                                                                                                        |
| **OriginalFilename** | Nome originale del file, senza includere un percorso. Queste informazioni consentono a un'applicazione di determinare se un file è stato rinominato da un utente. Il formato del nome dipende dal nome file system per cui è stato creato il file. Questa stringa è obbligatoria.                                                 |
| **PrivateBuild**     | Informazioni su una versione privata del file, ad esempio "Built by TESTER1 on \\ TESTBED". Questa stringa deve essere presente solo se **VS \_ FF \_ PRIVATEBUILD** è specificato nel *parametro fileflags* del blocco radice.                                                                                   |
| **ProductName**      | Nome del prodotto con cui viene distribuito il file. Questa stringa è obbligatoria.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versione del prodotto con cui viene distribuito il file, ad esempio "3.10" o "5.00.RC2". Questa stringa è obbligatoria.                                                                                                                                                                                       |
| **SpecialBuild**     | Testo che indica le differenze tra questa versione del file e la versione standard, ad esempio "Build privata per TESTER1 che risolve i problemi del mouse nei computer M250 e M250E". Questa stringa deve essere presente solo se **VS \_ FF \_ SPECIALBUILD** è specificato nel *parametro fileflags* del blocco radice. |



 

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [Attributi comuni delle risorse.](common-resource-attributes.md)

## <a name="examples"></a>Esempio

L'esempio seguente definisce una **risorsa VERSIONINFO:**

``` syntax
#define VER_FILEVERSION             3,10,349,0
#define VER_FILEVERSION_STR         "3.10.349.0\0"

#define VER_PRODUCTVERSION          3,10,0,0
#define VER_PRODUCTVERSION_STR      "3.10\0"

#ifndef DEBUG
#define VER_DEBUG                   0
#else
#define VER_DEBUG                   VS_FF_DEBUG
#endif

VS_VERSION_INFO VERSIONINFO
FILEVERSION     VER_FILEVERSION
PRODUCTVERSION  VER_PRODUCTVERSION
FILEFLAGSMASK   VS_FFI_FILEFLAGSMASK
FILEFLAGS       (VER_PRIVATEBUILD|VER_PRERELEASE|VER_DEBUG)
FILEOS          VOS__WINDOWS32
FILETYPE        VFT_DLL
FILESUBTYPE     VFT2_UNKNOWN
BEGIN
    BLOCK "StringFileInfo"
    BEGIN
        BLOCK "040904E4"
        BEGIN
            VALUE "CompanyName",      VER_COMPANYNAME_STR
            VALUE "FileDescription",  VER_FILEDESCRIPTION_STR
            VALUE "FileVersion",      VER_FILEVERSION_STR
            VALUE "InternalName",     VER_INTERNALNAME_STR
            VALUE "LegalCopyright",   VER_LEGALCOPYRIGHT_STR
            VALUE "LegalTrademarks1", VER_LEGALTRADEMARKS1_STR
            VALUE "LegalTrademarks2", VER_LEGALTRADEMARKS2_STR
            VALUE "OriginalFilename", VER_ORIGINALFILENAME_STR
            VALUE "ProductName",      VER_PRODUCTNAME_STR
            VALUE "ProductVersion",   VER_PRODUCTVERSION_STR
        END
    END

    BLOCK "VarFileInfo"
    BEGIN
        /* The following line should only be modified for localized versions.     */
        /* It consists of any number of WORD,WORD pairs, with each pair           */
        /* describing a language,codepage combination supported by the file.      */
        /*                                                                        */
        /* For example, a file might have values "0x409,1252" indicating that it  */
        /* supports English language (0x409) in the Windows ANSI codepage (1252). */

        VALUE "Translation", 0x409, 1252

    END
END
```

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Uso delle informazioni sulla versione](./using-version-information.md)
</dt> <dt>

[Informazioni sulla versione](./version-information.md)
</dt> </dl>

 

 