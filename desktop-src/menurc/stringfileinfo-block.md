---
title: Istruzione BLOCK StringFileInfo
description: Descrive il formato del blocco di informazioni sulla stringa.
ms.assetid: d5edf638-b70a-44d0-a43a-89d4d21e679f
keywords:
- Menu e altre risorse dell'istruzione BLOCK StringFileInfo
topic_type:
- apiref
api_name:
- StringFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468257d0b8b8b53f3168e8e11e2f649b8354d50a76d3c2a010b98d245472aad0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119886767"
---
# <a name="stringfileinfo-block-statement"></a>Istruzione BLOCK StringFileInfo

Definisce un blocco di informazioni di stringa.

``` syntax
BLOCK "StringFileInfo" { BLOCK "lang-charset" {VALUE "string-name", "value" . . . }}
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="lang-charset"></span><span id="LANG-CHARSET"></span>*lang-charset*
</dt> <dd>

Coppia di identificatori di lingua e set di caratteri. Si tratta di una stringa esadecimale costituita dalla concatenazione degli identificatori di lingua e set di caratteri specificati nella sezione Osservazioni.

</dd> <dt>

<span id="string-name"></span><span id="STRING-NAME"></span>*string-name*
</dt> <dd>

Nome di un valore nel blocco e può essere uno dei nomi predefiniti specificati nella sezione Osservazioni.

</dd> <dt>

<span id="value"></span><span id="VALUE"></span>*Valore*
</dt> <dd>

Stringa di caratteri che specifica il valore del nome della stringa corrispondente. È possibile specificare **più di** un'istruzione VALUE.

</dd> </dl>

## <a name="remarks"></a>Commenti

Il *parametro lang-charset* specifica uno dei codici di lingua seguenti.



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
| 0x0414 | Norvegese - Bokmal  | 0x100C | Francese svizzero              |
| 0x0810 | Italiano (Svizzera)       | 0x0816 | Portoghese (Portogallo)     |
| 0x0813 | Olandese (Olandese)       | 0x081A | Serbo-Croatian (alfabeto cirillico) |
| 0x0814 | Norvegese - Nynorsk | ?      | ?                         |



 

Il *parametro lang-charset* specifica anche uno degli identificatori di set di caratteri seguenti.



| Identificatore | Set di caratteri              |
|------------|----------------------------|
| 0          | ASCII a 7 bit                |
| 932        | Giappone (Shift – JIS X-0208) |
| 949        | Corea del Sud (MAIUSC - KSC 5601)   |
| 950        | Taiwan (Big5)              |
| 1200       | Unicode                    |
| 1250       | Latin-2 (Europa orientale) |
| 1251       | Cirillico                   |
| 1252       | Multilingue               |
| 1253       | Greco                      |
| 1254       | Turco                    |
| 1255       | Ebraico                     |
| 1256       | Arabo                     |



 

Il *parametro string-name* specifica uno dei nomi predefiniti seguenti.



| Nome                 | Descrizione                                                                                                                                                                                                                                                                                                 |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Commenti**         | Informazioni aggiuntive che devono essere visualizzate a scopo diagnostico.                                                                                                                                                                                                                                    |
| **CompanyName**      | Società che ha prodotto il file, ad esempio "Microsoft Corporation" o "Standard Microsystems Corporation, Inc." Questa stringa è obbligatoria.                                                                                                                                                                   |
| **FileDescription**  | Descrizione del file da presentare agli utenti. Questa stringa può essere visualizzata in una casella di riepilogo quando l'utente sceglie i file da installare, ad esempio "Keyboard Driver for AT-Style Keyboards". Questa stringa è obbligatoria.                                                                                            |
| **FileVersion**      | Numero di versione del file, ad esempio "3.10" o "5.00.RC2". Questa stringa è obbligatoria.                                                                                                                                                                                                                      |
| **InternalName**     | Nome interno del file, se presente, ad esempio un nome di modulo se il file è una libreria a collegamento dinamico. Se il file non ha un nome interno, questa stringa deve essere il nome file originale, senza estensione. Questa stringa è obbligatoria.                                                                       |
| **LegalCopyright**   | Informazioni sul copyright che si applicano al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, le date di copyright e così via. Questa stringa è facoltativa.                                                                                                                                             |
| **LegalTrademarks**  | Marchi e marchi registrati applicabili al file. Deve includere il testo completo di tutte le comunicazioni, i simboli legali, i numeri dei marchi e così via. Questa stringa è facoltativa.                                                                                                                        |
| **OriginalFilename** | Nome originale del file, senza includere un percorso. Queste informazioni consentono a un'applicazione di determinare se un file è stato rinominato da un utente. Il formato del nome dipende dal nome file system per cui è stato creato il file. Questa stringa è obbligatoria.                                                 |
| **PrivateBuild**     | Informazioni su una versione privata del file, ad esempio "Compilato da TESTER1 in \\ TESTBED". Questa stringa deve essere presente solo se **VS \_ FF \_ PRIVATEBUILD** è specificato nel *parametro fileflags* del blocco radice.                                                                                   |
| **ProductName**      | Nome del prodotto con cui viene distribuito il file. Questa stringa è obbligatoria.                                                                                                                                                                                                                            |
| **ProductVersion**   | Versione del prodotto con cui viene distribuito il file, ad esempio "3.10" o "5.00.RC2". Questa stringa è obbligatoria.                                                                                                                                                                                       |
| **SpecialBuild**     | Testo che specifica le differenze tra questa versione del file e la versione standard, ad esempio "Build privata per TESTER1 che risolve i problemi del mouse nei computer M250 e M250E". Questa stringa deve essere presente solo se **VS \_ FF \_ SPECIALBUILD** è specificato nel *parametro fileflags* del blocco radice. |



 

 

 




