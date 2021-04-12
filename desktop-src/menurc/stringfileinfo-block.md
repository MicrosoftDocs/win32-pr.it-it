---
title: Istruzione BLOCK StringFileInfo
description: Descrive il formato del blocco di informazioni sulle stringhe.
ms.assetid: d5edf638-b70a-44d0-a43a-89d4d21e679f
keywords:
- Menu di istruzioni di blocco StringFileInfo e altre risorse
topic_type:
- apiref
api_name:
- StringFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb0a1c5e7a2fd5e3d2f096c882ca928ce1febf92
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104397734"
---
# <a name="stringfileinfo-block-statement"></a>Istruzione BLOCK StringFileInfo

Definisce un blocco di informazioni sulle stringhe.

``` syntax
BLOCK "StringFileInfo" { BLOCK "lang-charset" {VALUE "string-name", "value" . . . }}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lang-charset"></span><span id="LANG-CHARSET"></span>*lang-charset*
</dt> <dd>

Coppia di lingua e identificatore del set di caratteri. Si tratta di una stringa esadecimale costituita dalla concatenazione degli identificatori del linguaggio e del set di caratteri specificati nella sezione Osservazioni.

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*nome stringa*
</dt> <dd>

Nome di un valore nel blocco. può essere uno dei nomi predefiniti specificati nella sezione Osservazioni.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*valore*
</dt> <dd>

Stringa di caratteri che specifica il valore del nome della stringa corrispondente. È possibile assegnare più di un'istruzione **value** .

</dd> </dl>

## <a name="remarks"></a>Commenti

Il parametro *lang-charset* specifica uno dei seguenti codici di lingua.



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
| 0x0414 | Norvegese – Bokmal  | 0x100C | Francese svizzero              |
| 0x0810 | Italiano svizzero       | 0x0816 | Portoghese (Portogallo)     |
| 0x0813 | Olandese belga       | 0x081A | Serbo-Croatian (alfabeto cirillico) |
| 0x0814 | Norvegese – Nynorsk | ?      | ?                         |



 

Il parametro *lang-charset* specifica anche uno dei seguenti identificatori di set di caratteri.



| Identificatore | Set di caratteri              |
|------------|----------------------------|
| 0          | ASCII a 7 bit                |
| 932        | Giappone (MAIUSC – JIS X-0208) |
| 949        | Corea (Shift – KSC 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latino 2 (Europa orientale) |
| 1251       | Cirillico                   |
| 1252       | Multilingue               |
| 1253       | Greco                      |
| 1254       | Turco                    |
| 1255       | Ebraico                     |
| 1256       | Arabo                     |



 

Il parametro *String-name* specifica uno dei seguenti nomi predefiniti.



| Nome                 | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Commenti**         | Informazioni aggiuntive da visualizzare per scopi diagnostici.                                                                                                                                                                                                                                    |
| **CompanyName**      | Società che ha prodotto il file, ad esempio "Microsoft Corporation" o "Standard Microsystems Corporation, Inc." Questa stringa è obbligatoria.                                                                                                                                                                   |
| **FileDescription**  | Descrizione del file da presentare agli utenti. Questa stringa può essere visualizzata in una casella di riepilogo quando l'utente sceglie i file da installare, ad esempio "driver tastiera per AT-Style tastiere". Questa stringa è obbligatoria.                                                                                            |
| **FileVersion**      | Numero di versione del file, ad esempio "3,10" o "5.00. RC2". Questa stringa è obbligatoria.                                                                                                                                                                                                                      |
| **InternalName**     | Nome interno del file, se ne esiste uno, ad esempio un nome di modulo se il file è una libreria a collegamento dinamico. Se il file non ha un nome interno, la stringa deve essere il nome file originale, senza estensione. Questa stringa è obbligatoria.                                                                       |
| **LegalCopyright**   | Note sul copyright applicabili al file. Questo deve includere il testo completo di tutte le comunicazioni, i simboli legali, le date di copyright e così via. Questa stringa è facoltativa.                                                                                                                                             |
| **LegalTrademarks**  | Marchi e marchi registrati applicabili al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, i numeri dei marchi e così via. Questa stringa è facoltativa.                                                                                                                        |
| **OriginalFilename** | Nome originale del file senza includere un percorso. Queste informazioni consentono a un'applicazione di determinare se un file è stato rinominato da un utente. Il formato del nome dipende dalla file system per cui è stato creato il file. Questa stringa è obbligatoria.                                                 |
| **PrivateBuild**     | Informazioni su una versione privata del file, ad esempio "compilata da TESTER1 su \\ banco di controllo". Questa stringa deve essere presente solo se **vs \_ FF \_ PRIVATEBUILD** è specificato nel parametro *FILEFLAGS* del blocco radice.                                                                                   |
| **ProductName**      | Nome del prodotto con cui viene distribuito il file. Questa stringa è obbligatoria.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versione del prodotto con cui viene distribuito il file, ad esempio "3,10" o "5.00. RC2". Questa stringa è obbligatoria.                                                                                                                                                                                       |
| **SpecialBuild**     | Testo che specifica la differenza di questa versione del file rispetto alla versione standard, ad esempio "compilazione privata per TESTER1 risoluzione dei problemi del mouse nei computer M250 e M250E". Questa stringa deve essere presente solo se **vs \_ FF \_ SPECIALBUILD** è specificato nel parametro *FILEFLAGS* del blocco radice. |



 

 

 




