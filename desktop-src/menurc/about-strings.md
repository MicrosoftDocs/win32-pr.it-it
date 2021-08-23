---
title: Informazioni sulle stringhe
description: In questo argomento vengono illustrate le funzioni stringa.
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- risorse, stringhe
- stringhe
- funzioni per i valori stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d50f47205ec021bffaa4cb6e24aa4825177a3fc0d8546f3a14b1d4b0e0ca4271
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119034389"
---
# <a name="about-strings"></a>Informazioni sulle stringhe

Le funzioni stringa offrono alle applicazioni i mezzi per copiare, confrontare, ordinare, formattare e convertire stringhe di caratteri, nonché i mezzi per determinare il tipo di carattere di ogni carattere in una stringa. Tutte le funzioni stringa supportano i set di caratteri a byte singolo, a byte doppio e Unicode se questi set di caratteri sono supportati dal sistema operativo in cui viene eseguita l'applicazione.

**Avviso di sicurezza:** L'uso non corretto delle funzioni stringa può causare problemi di sicurezza per l'applicazione. In genere si tratta di un sovraccarico del buffer che può consentire un attacco Denial of Service contro l'applicazione o l'inserimento di codice eseguibile da parte di un utente malintenzionato. Le funzioni Strsafe consentono una gestione più sicura delle stringhe e sono consigliate per una maggiore sicurezza per l'applicazione. Per altre informazioni su queste funzioni, vedere [Uso delle funzioni Strsafe.h](strsafe-ovw.md).

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Confronto con le funzioni stringa Run-Time C](#comparison-with-c-run-time-string-functions)
-   [Risorse stringa](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>Confronto con le funzioni stringa Run-Time C

Molte funzioni stringa duplicano o migliorano le funzioni stringa familiari della libreria di runtime C standard (CRT). Molti dei miglioramenti consentono alle funzioni stringa di funzionare con i set di caratteri Unicode o estesi. La tabella seguente illustra le funzioni CRT, le funzioni Windows (che supportano Unicode, a differenza delle funzioni CRT) e le funzioni StrSafe.



| Funzione stringa CRT                                       | Windows Funzione String    | Funzione StrSafe                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [Strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**lstrcmp**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | (nessuna funzione equivalente)                                                                                                                                                                                                                                                                                                                                                                                  |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

La funzione **strlen,** ad esempio, restituisce sempre il numero di byte in una stringa, ma la funzione [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) restituisce il numero di valori **TCHAR,** che fa riferimento ai byte per le versioni ANSI della funzione o ai valori **WCHAR** per le versioni Unicode.

Le funzioni stringa seguenti differiscono dalle funzioni C standard, ad esempio **tolower** e **toupper,** in quanto operano su qualsiasi carattere in un set di caratteri. Usando la funzione [**CharLower,**](/windows/desktop/api/Winuser/nf-winuser-charlowera) ad esempio, un'applicazione può convertire un U maiuscolo con umlaut (Ü) in minuscolo (ü). Per altre informazioni sui set di caratteri, vedere [Set di caratteri a byte singolo](/windows/desktop/Intl/single-byte-character-sets).



| Funzione                               | Descrizione                                   |
|----------------------------------------|-----------------------------------------------|
| [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | Converte un carattere o una stringa in lettere minuscole.  |
| [**CharLowerBuff**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | Converte una stringa di caratteri in lettere minuscole.     |
| [**CharNext**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | Passa al carattere successivo in una stringa.      |
| [**CharPrev**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | Passa al carattere precedente in una stringa. |
| [**CharUpper**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | Converte un carattere o una stringa in lettere maiuscole.  |
| [**CharUpperBuff**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | Converte una stringa in lettere maiuscole.               |



 

Le funzioni stringa seguenti determinano un carattere in base alla semantica della lingua selezionata dall'utente. Queste funzioni sono abilitate per Unicode.



| Funzione                                         | Descrizione                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**IsCharAlpha**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | Determina se un carattere è alfabetico.   |
| [**IsCharAlphaNumeric**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | Determina se un carattere è alfanumerico. |
| [**IsCharLower**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | Determina se un carattere è minuscolo.    |
| [**IsCharUpper**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | Determina se un carattere è maiuscolo.    |



 

La tabella seguente illustra le estensioni Unicode per le funzioni di run-time C standard (CRT). Come accennato in precedenza, le funzioni StrSafe consentono una gestione più sicura delle stringhe e sono consigliate per una maggiore sicurezza per l'applicazione.



| Funzione CRT standard                                       | Funzione String                | Funzione StrSafe                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>Risorse stringa

Un'applicazione che gestisce stringhe di caratteri nelle risorse può essere convertita in nuove lingue con il minimo sforzo. Anziché cercare stringhe nei moduli di origine, è sufficiente tradurre le stringhe nel file di risorse e ricollegare l'applicazione. Inoltre, l'uso di risorse stringa semplifica la creazione di versioni Unicode e non Unicode dell'applicazione dagli stessi file di origine.

La [**funzione LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa) carica una risorsa stringa dal file eseguibile di un'applicazione. La [**funzione FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) carica una risorsa stringa e interpreta le opzioni di formattazione che possono essere incorporate nella stringa.

Le risorse in formato binario vengono archiviate in formato Unicode. Quando si caricano risorse, le applicazioni possono usare la versione Unicode delle funzioni di risorsa ([**LoadStringW**](/windows/desktop/api/Winuser/nf-winuser-loadstringa), ad esempio) per ottenere le risorse come dati Unicode.

Per le risorse stringa a 16 bit, la lunghezza massima è 255 caratteri. Per le risorse stringa a 32 bit, la lunghezza massima è 65535 caratteri.

 

 