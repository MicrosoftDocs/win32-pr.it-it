---
title: Risorsa VERSIONINFO
description: Definisce una risorsa di informazioni sulla versione. La risorsa contiene informazioni sul file come numero di versione, il sistema operativo previsto e il nome file originale. La risorsa deve essere utilizzata con le funzioni di informazioni sulla versione.
ms.assetid: be4fbf3d-ca30-4de1-b17a-691a316edfad
keywords:
- Menu risorse VERSIONINFO e altre risorse
topic_type:
- apiref
api_name:
- VERSIONINFO
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9248abe18d07820ebefaa6d939f36f617f6cd07f
ms.sourcegitcommit: 25e1fa2b3641ae13b79e0afdf9cb7a168d99e009
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/16/2020
ms.locfileid: "104339579"
---
# <a name="versioninfo-resource"></a>Risorsa VERSIONINFO

Definisce una risorsa di informazioni sulla versione. La risorsa contiene informazioni sul file come numero di versione, il sistema operativo previsto e il nome file originale. La risorsa deve essere utilizzata con le funzioni di [informazioni sulla versione](./version-information.md) .

Esistono due modi per formattare un'istruzione **VERSIONINFO** :

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

<span id="versionID"></span><span id="versionid"></span><span id="VERSIONID"></span>*versionID*
</dt> <dd>

Identificatore della risorsa di informazioni sulla versione. Questo valore deve essere 1.

</dd> <dt>

<span id="fixed-info"></span><span id="FIXED-INFO"></span>*Fixed-info*
</dt> <dd>

Informazioni sulla versione, ad esempio la versione del file e il sistema operativo desiderato. Questo parametro è costituito dalle istruzioni seguenti.



| Istruzione                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *Versione* **fileversion**         | Numero di versione binario del file. La *versione* è costituita da integer a 2 32 bit, definiti da integer a 4 16 bit. Ad esempio, "FileVersion 3, 10, 0, 61" viene convertito in due parole doppie: 0x0003000a e 0x0000003D, in questo ordine. Di conseguenza, se la *versione* è definita dai valori **DWORD** *DW1* e *DW2*, è necessario che vengano visualizzati nell'istruzione **fileversion** nel modo seguente: `HIWORD(dw1)` , `LOWORD(dw1)` , `HIWORD(dw2)` , `LOWORD(dw2)` . |
|  *Versione* di ProductVersion      | Numero di versione binario per il prodotto con cui il file viene distribuito. Il parametro *Version* è integer a 2 32 bit, definiti da integer a 4 16 bit. Per ulteriori informazioni sulla *versione*, vedere la descrizione di **fileversion** .                                                                                                                                                                                                           |
|  *FILEFLAGSMASK* FILEFLAGSMASK | Indica i bit nell'istruzione **FILEflags** validi. Per Windows a 16 bit, questo valore è 0x3F.                                                                                                                                                                                                                                                                                                                                          |
| *Flag* **fileflag** FILEFLAGS         | Attributi del file.                                                                                                                                                                                                                                                                                                                                                                                                                         |
| *FILEOS* di **FILEOS**               | Sistema operativo per il quale è stato progettato questo file. Il parametro *FILEOS* può essere uno dei valori del sistema operativo specificati nella sezione Osservazioni.                                                                                                                                                                                                                                                                                               |
| **FileType**  filetype           | Tipo generale di file. Il parametro *FileType* può essere uno dei valori dei tipi di file elencati nella sezione Osservazioni.                                                                                                                                                                                                                                                                                                                                |
| Sottotipo **FILESUBTYPE**          | Funzione del file. Il parametro del *sottotipo* è zero a meno che il parametro *FileType* **nell'istruzione filetype non** sia VFT \_ drv, VFT \_ font o VFT \_ vxd. Per un elenco di valori dei sottotipi di file, vedere la sezione Osservazioni.                                                                                                                                                                                                                            |



 

</dd> <dt>

<span id="block-statement"></span><span id="BLOCK-STATEMENT"></span>*Block-Statement*
</dt> <dd>

Specifica uno o più blocchi di informazioni sulla versione. Un blocco può contenere informazioni sulle stringhe o informazioni sulle variabili. Per altre informazioni, vedere blocco [**StringFileInfo**](stringfileinfo-block.md) o [**VarFileInfo**](varfileinfo-block.md).

</dd> </dl>

## <a name="remarks"></a>Commenti

Per usare le costanti specificate con l'istruzione **VERSIONINFO** , è necessario includere il file di intestazione winver. h o Windows. h nel file di definizione delle risorse.

Nell'elenco seguente vengono descritti i parametri utilizzati nell'istruzione **VERSIONINFO** :

<dl> <dt>

<span id="fileflags"></span><span id="FILEFLAGS"></span>*FILEFLAGS*
</dt> <dd>

Una combinazione dei valori seguenti.



| Valore                      | Descrizione                                                                                                                                                                                                                                                                 |
|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **DEBUG di VS \_ FF \_**          | Il file contiene informazioni di debug o è compilato con funzionalità di debug abilitate.                                                                                                                                                                                         |
| **con \_ patch di vs FF \_**        | Il file è stato modificato e non è identico al file di spedizione originale con lo stesso numero di versione.                                                                                                                                                                       |
| **\_ \_ versione preliminare di vs FF**     | Il file è una versione di sviluppo, non un prodotto rilasciato commercialmente.                                                                                                                                                                                                         |
| **VS \_ FF \_ PRIVATEBUILD**   | Il file non è stato compilato con procedure di rilascio standard. Se questo valore viene specificato, il [**blocco StringFileInfo**](stringfileinfo-block.md) deve contenere una stringa **PrivateBuild** .                                                                                              |
| **VS \_ FF \_ SPECIALBUILD**   | Il file è stato compilato dall'azienda originale usando le procedure di rilascio standard, ma è una variante del file standard con lo stesso numero di versione. Se questo valore viene specificato, il blocco del [blocco **StringFileInfo**](stringfileinfo-block.md) deve contenere una stringa **SpecialBuild** . |
| **VS \_ \_ FILEFLAGSMASK** | Combinazione di tutti i valori precedenti.                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span id="fileos"></span><span id="FILEOS"></span>*FILEOS*
</dt> <dd>

Uno dei valori seguenti.



| Valore                   | Descrizione                                                      |
|-------------------------|------------------------------------------------------------------|
| **VOS \_ sconosciuto**        | Il sistema operativo per il quale è stato progettato il file è sconosciuto. |
| **\_DOS vos**            | Il file è stato progettato per MS-DOS.                                    |
| **VOS \_ NT**             | Il file è stato progettato per Windows a 32 bit.                            |
| **\_ \_ WINDOWS16 vos**    | Il file è stato progettato per Windows a 16 bit.                            |
| **\_ \_ WINDOWS32 vos**    | Il file è stato progettato per Windows a 32 bit.                            |
| **VOS \_ DOS \_ WINDOWS16** | Il file è stato progettato per Windows a 16 bit in esecuzione con MS-DOS.        |
| **VOS \_ DOS \_ WINDOWS32** | Il file è stato progettato per Windows a 32 bit in esecuzione con MS-DOS.        |
| **VOS \_ NT \_ WINDOWS32**  | Il file è stato progettato per Windows a 32 bit.                            |



 

I valori 0x00002L, 0x00003L, 0x20000L e 0x30000L sono riservati.

</dd> <dt>

<span id="filetype"></span><span id="FILETYPE"></span>*filetype*
</dt> <dd>

Uno dei valori seguenti.



| Valore                | Descrizione                                                                                                                 |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| **VFT \_ sconosciuto**     | Tipo di file sconosciuto.                                                                                                       |
| **\_app VFT**         | Il file contiene un'applicazione.                                                                                               |
| **\_dll VFT**         | Il file contiene una libreria di collegamento dinamico (DLL).                                                                                 |
| **VFT \_ drv**         | Il file contiene un driver di dispositivo. Se *FileType è* **VFT \_ drv**, il *sottotipo* contiene una descrizione più specifica del driver. |
| **\_tipo di carattere VFT**        | Il file contiene un tipo di carattere. Se *FileType* è \_ un tipo di carattere VFT, il *sottotipo* contiene una descrizione più specifica del tipo di carattere.               |
| **\_vxd VFT**         | Il file contiene un dispositivo virtuale.                                                                                             |
| **\_lib VFT statica \_** | Il file contiene una libreria a collegamento statico.                                                                                        |



 

Tutti gli altri valori sono riservati per l'utilizzo da Microsoft.

</dd> <dt>

<span id="subtype"></span><span id="SUBTYPE"></span>*sottotipo*
</dt> <dd>

Informazioni aggiuntive sul tipo di file.

Se *FileType* specifica **VFT \_ drv**, questo parametro può essere uno dei valori seguenti.



| Valore                             | Descrizione                               |
|-----------------------------------|-------------------------------------------|
| **VFT2 \_ sconosciuto**                 | Il tipo di driver è sconosciuto.                   |
| **VFT2 \_ drv \_ comm**               | Il file contiene un driver di comunicazione.    |
| **\_Stampante VFT2 DRV \_**            | Il file contiene un driver della stampante.           |
| **\_Tastiera VFT2 DRV \_**           | Il file contiene un driver della tastiera.          |
| **\_Linguaggio VFT2 DRV \_**           | Il file contiene un driver di linguaggio.          |
| **\_Visualizzazione VFT2 DRV \_**            | Il file contiene un driver di visualizzazione.           |
| **\_Mouse VFT2 DRV \_**              | Il file contiene un driver del mouse.             |
| **\_Rete VFT2 DRV \_**            | Il file contiene un driver di rete.           |
| **\_Sistema DRV \_ VFT2**             | Il file contiene un driver di sistema.            |
| **VFT2 \_ drv \_ installabile**        | Il file contiene un driver installabile.      |
| **VFT2 \_ drv \_ audio**              | Il file contiene un driver audio.             |
| **\_Stampante VFT2 DRV con \_ versione \_** | Il file contiene un driver della stampante con versione. |



 

Se *FileType* specifica il **\_ tipo di carattere VFT**, questo parametro può essere uno dei valori seguenti.



| Valore                    | Descrizione                    |
|--------------------------|--------------------------------|
| **VFT2 \_ sconosciuto**        | Il tipo di carattere è sconosciuto.          |
| **\_Raster carattere \_ VFT2**   | Il file contiene un tipo di carattere raster.   |
| **\_Vettore del tipo di carattere VFT2 \_**   | Il file contiene un tipo di carattere vettoriale.   |
| **\_Tipo di carattere VFT2 \_ TrueType** | Il file contiene un tipo di carattere TrueType. |



 

Se *FileType* specifica VFT \_ vxd, questo parametro deve corrispondere all'identificatore del dispositivo virtuale incluso nel blocco di controllo del dispositivo virtuale.

Tutti i valori dei *sottotipi* non elencati sono riservati per l'utilizzo da Microsoft.

</dd> <dt>

<span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*
</dt> <dd>

Uno dei seguenti codici di lingua.



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
| 0x040A | Spagnolo castigliano   | 0x041E | Thai                      |
| 0x040B | Finlandese             | 0x041F | Turco                   |
| 0x040C | Francese              | 0x0420 | Urdu                      |
| 0x040D | Ebraico              | 0x0421 | Bahasa                    |
| 0x040E | Ungherese           | 0x0804 | Cinese semplificato        |
| 0x040F | Islandese           | 0x0807 | Tedesco svizzero              |
| 0x0410 | Italiano             | 0x0809 | Regno Unito. Inglese              |
| 0x0411 | Giapponese            | 0x080A | Spagnolo (Messico)          |
| 0x0412 | Coreano              | 0x080C | Francese belga            |
| 0x0413 | Olandese               | 0x0C0C | Francese (Canada)           |
| 0x0414 | Norvegese? Bokmal  | 0x100C | Francese svizzero              |
| 0x0810 | Italiano svizzero       | 0x0816 | Portoghese (Portogallo)     |
| 0x0813 | Olandese belga       | 0x081A | Serbo-Croatian (alfabeto cirillico) |
| 0x0814 | Norvegese? Nynorsk |        |                           |



 

</dd> <dt>

<span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*
</dt> <dd>

Uno dei seguenti identificatori di set di caratteri.



| Decimal | Valore esadecimale | Set di caratteri              |
|---------|-------------|----------------------------|
| 0       | 0000        | ASCII a 7 bit                |
| 932     | 03A4        | Giappone (turno? JIS X-0208) |
| 949     | 03B5        | Corea (Shift? KSC 5601)   |
| 950     | 03B6        | Taiwan (Big5)              |
| 1200    | 04B0        | Unicode                    |
| 1250    | 04E2        | Latino 2 (Europa orientale) |
| 1251    | 04E3        | Cirillico                   |
| 1252    | 04E4        | Multilingue               |
| 1253    | 04E5        | Greco                      |
| 1254    | 04E6        | Turco                    |
| 1255    | 04E7        | Ebraico                     |
| 1256    | 04E8        | Arabo                     |



 

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*nome stringa*
</dt> <dd>

Uno dei seguenti nomi predefiniti.



| Nome                 | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Commenti**         | Informazioni aggiuntive da visualizzare per scopi diagnostici.                                                                                                                                                                                                                                    |
| **CompanyName**      | Società che ha prodotto il file? ad esempio, "Microsoft Corporation" o "Standard Microsystems Corporation, Inc." Questa stringa è obbligatoria.                                                                                                                                                                   |
| **FileDescription**  | Descrizione del file da presentare agli utenti. Questa stringa può essere visualizzata in una casella di riepilogo quando l'utente sceglie i file da installare, ad esempio "driver tastiera per AT-Style tastiere". Questa stringa è obbligatoria.                                                                                            |
| **FileVersion**      | Numero di versione del file, ad esempio "3,10" o "5.00. RC2". Questa stringa è obbligatoria.                                                                                                                                                                                                                      |
| **InternalName**     | Nome interno del file, se presente? ad esempio, un nome di modulo se il file è una libreria a collegamento dinamico. Se il file non ha un nome interno, la stringa deve essere il nome file originale, senza estensione. Questa stringa è obbligatoria.                                                                       |
| **LegalCopyright**   | Note sul copyright applicabili al file. Questo deve includere il testo completo di tutte le comunicazioni, i simboli legali, le date di copyright e così via. Questa stringa è facoltativa.                                                                                                                                             |
| **LegalTrademarks**  | Marchi e marchi registrati applicabili al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, i numeri dei marchi e così via. Questa stringa è facoltativa.                                                                                                                        |
| **OriginalFilename** | Nome originale del file senza includere un percorso. Queste informazioni consentono a un'applicazione di determinare se un file è stato rinominato da un utente. Il formato del nome dipende dalla file system per cui è stato creato il file. Questa stringa è obbligatoria.                                                 |
| **PrivateBuild**     | Informazioni su una versione privata del file, ad esempio "compilato da TESTER1 su banco di controllo \\ ". Questa stringa deve essere presente solo se **vs \_ FF \_ PRIVATEBUILD** è specificato nel parametro *FILEFLAGS* del blocco radice.                                                                                   |
| **ProductName**      | Nome del prodotto con cui viene distribuito il file. Questa stringa è obbligatoria.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versione del prodotto con cui viene distribuito il file, ad esempio "3,10" o "5.00. RC2". Questa stringa è obbligatoria.                                                                                                                                                                                       |
| **SpecialBuild**     | Testo che indica la differenza tra la versione del file e la versione standard, ad esempio "compilazione privata per TESTER1 risoluzione dei problemi del mouse nei computer M250 e M250E". Questa stringa deve essere presente solo se **vs \_ FF \_ SPECIALBUILD** è specificato nel parametro *FILEFLAGS* del blocco radice. |



 

</dd> </dl>

Alcuni attributi sono supportati anche per la compatibilità con le versioni precedenti. Per altre informazioni, vedere [attributi di risorse comuni](common-resource-attributes.md).

## <a name="examples"></a>Esempio

Nell'esempio seguente viene definita una risorsa **VERSIONINFO** :

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

[Utilizzo delle informazioni sulla versione](./using-version-information.md)
</dt> <dt>

[Informazioni sulla versione](./version-information.md)
</dt> </dl>

 

 