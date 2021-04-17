---
title: Informazioni sulle stringhe
description: In questo argomento vengono illustrate le funzioni di stringa.
ms.assetid: f1799fbf-4619-4b19-998e-b1d2f4c19a35
keywords:
- risorse, stringhe
- stringhe
- funzioni per i valori stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ff9fa6c9d93ba2f5c089b52b56816cad74bb61c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "106299685"
---
# <a name="about-strings"></a>Informazioni sulle stringhe

Le funzioni di stringa consentono alle applicazioni di copiare, confrontare, ordinare, formattare e convertire stringhe di caratteri, nonché di determinare il tipo di carattere di ogni carattere in una stringa. Tutte le funzioni stringa supportano i set di caratteri a byte singolo, a doppio byte e Unicode se questi set di caratteri sono supportati dal sistema operativo in cui viene eseguita l'applicazione.

**Avviso di sicurezza:** L'uso errato delle funzioni stringa può causare problemi di sicurezza per l'applicazione. Ciò comporta in genere un sovraccarico del buffer che può consentire un attacco di tipo Denial of Service contro l'applicazione o l'inserimento di codice eseguibile da un utente malintenzionato. Le funzioni strsafe consentono una gestione più sicura delle stringhe e sono consigliate per una maggiore sicurezza per l'applicazione. Per ulteriori informazioni su queste funzioni, vedere [utilizzo delle funzioni strsafe. h](strsafe-ovw.md).

In questa sezione vengono illustrati gli argomenti seguenti.

-   [Confronto con funzioni di stringa di Run-Time C](#comparison-with-c-run-time-string-functions)
-   [Risorse di stringa](#string-resources)

## <a name="comparison-with-c-run-time-string-functions"></a>Confronto con funzioni di stringa di Run-Time C

Molte funzioni stringa duplicano o migliorano le funzioni di stringa note dalla libreria di runtime C standard (CRT). Molti dei miglioramenti consentono alle funzioni stringa di funzionare con i set di caratteri Unicode o estesi. La tabella seguente illustra le funzioni CRT, le funzioni di Windows (che supportano Unicode, a differenza delle funzioni CRT) e le funzioni StrSafe.



| Funzione stringa CRT                                       | Funzione stringa Windows    | StrSafe (funzione)                                                                                                                                                                                                                                                                                                                                                                                          |
|-----------------------------------------------------------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [strcat](/cpp/c-runtime-library/reference/strcat-wcscat-mbscat?view=vs-2019) | [**lstrcat**](/windows/desktop/api/Winbase/nf-winbase-lstrcata) | <dl> <dt>[**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)</dt> <dt>[**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)</dt> <dt>[**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)</dt> <dt>[**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)</dt> </dl>         |
| [strcmp](/cpp/c-runtime-library/reference/strcmp-wcscmp-mbscmp?view=vs-2019) | [**LSTRCMP**](/windows/desktop/api/Winbase/nf-winbase-lstrcmpa) | (nessuna funzione equivalente)                                                                                                                                                                                                                                                                                                                                                                                  |
| [strcpy](/cpp/c-runtime-library/reference/strcpy-wcscpy-mbscpy?view=vs-2019) | [**lstrcpy**](/windows/desktop/api/Winbase/nf-winbase-lstrcpya) | <dl> <dt>[**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)</dt> <dt>[**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)</dt> <dt>[**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)</dt> <dt>[**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)</dt> </dl> |
| [strlen](/cpp/c-runtime-library/reference/strlen-wcslen-mbslen-mbslen-l-mbstrlen-mbstrlen-l?view=vs-2019) | [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) | <dl> <dt>[](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)</dt> <dt> [ **StringCbLength** StringCchLength](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)</dt> </dl>                                                                                                                                                                                       |



 

La funzione **strlen** , ad esempio, restituisce sempre il numero di byte in una stringa, ma la funzione [**lstrlen**](/windows/desktop/api/Winbase/nf-winbase-lstrlena) restituisce il numero di valori **TCHAR** , che fa riferimento a byte per le versioni ANSI della funzione o dei valori **WCHAR** per le versioni Unicode.

Le funzioni stringa seguenti sono diverse dalle funzioni C standard, ad esempio **ToLower** e **ToUpper** , in quanto operano su qualsiasi carattere in un set di caratteri. Utilizzando la funzione [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera) , ad esempio, un'applicazione può convertire un U maiuscolo con una dieresta (ü) in minuscolo (ü). Per ulteriori informazioni sui set di caratteri, vedere [set di caratteri a byte singolo](/windows/desktop/Intl/single-byte-character-sets).



| Funzione                               | Descrizione                                   |
|----------------------------------------|-----------------------------------------------|
| [**CharLower**](/windows/desktop/api/Winuser/nf-winuser-charlowera)         | Converte un carattere o una stringa in caratteri minuscoli.  |
| [**CharLowerBuff**](/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa) | Converte una stringa di caratteri in lettere minuscole.     |
| [**CharNext**](/windows/desktop/api/Winuser/nf-winuser-charnexta)           | Passa al carattere successivo in una stringa.      |
| [**CharPrev**](/windows/desktop/api/Winuser/nf-winuser-charpreva)           | Passa al carattere precedente in una stringa. |
| [**CharUpper**](/windows/desktop/api/Winuser/nf-winuser-charuppera)         | Converte un carattere o una stringa in lettere maiuscole.  |
| [**CharUpperBuff**](/windows/desktop/api/Winuser/nf-winuser-charupperbuffa) | Converte una stringa in lettere maiuscole.               |



 

Le funzioni stringa seguenti determinano la definizione di un carattere in base alla semantica della lingua selezionata dall'utente. Queste funzioni sono abilitate per Unicode.



| Funzione                                         | Descrizione                                     |
|--------------------------------------------------|-------------------------------------------------|
| [**IsCharAlpha**](/windows/desktop/api/Winuser/nf-winuser-ischaralphaa)               | Determina se un carattere è alfabetico.   |
| [**IsCharAlphaNumeric**](/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica) | Determina se un carattere è alfanumerico. |
| [**IsCharLower**](/windows/desktop/api/Winuser/nf-winuser-ischarlowera)               | Determina se un carattere è minuscolo.    |
| [**IsCharUpper**](/windows/desktop/api/Winuser/nf-winuser-ischaruppera)               | Determina se un carattere è in maiuscolo.    |



 

Nella tabella seguente vengono illustrate le estensioni Unicode per le funzioni di runtime del linguaggio C standard (CRT). Come indicato in precedenza, le funzioni StrSafe consentono una gestione più sicura delle stringhe e sono consigliate per una maggiore sicurezza per l'applicazione.



| Funzione CRT standard                                       | Funzione String                | StrSafe (funzione)                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------------------------------|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [sprintf](/cpp/c-runtime-library/reference/sprintf-sprintf-l-swprintf-swprintf-l-swprintf-l?view=vs-2019)  | [**wsprintf**](/windows/desktop/api/Winuser/nf-winuser-wsprintfa)   | <dl> <dt>[**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)</dt> <dt>[**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)</dt> <dt>[**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)</dt> <dt>[**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)</dt> </dl>         |
| [vsprintf](/cpp/c-runtime-library/reference/vsprintf-vsprintf-l-vswprintf-vswprintf-l-vswprintf-l?view=vs-2019) | [**wvsprintf**](/windows/desktop/api/Winuser/nf-winuser-wvsprintfa) | <dl> <dt>[**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)</dt> <dt>[**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa)</dt> <dt>[**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)</dt> <dt>[**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)</dt> </dl> |



 

## <a name="string-resources"></a>Risorse di stringa

Un'applicazione che mantiene le stringhe di caratteri nelle risorse può essere convertita in nuovi linguaggi con il minimo sforzo. Anziché cercare stringhe nei moduli di origine, è possibile tradurre semplicemente le stringhe nel file di risorse e ricollegare l'applicazione. Inoltre, l'utilizzo delle risorse di tipo stringa semplifica la creazione di versioni Unicode e non Unicode dell'applicazione dagli stessi file di origine.

La funzione [**LoadString**](/windows/desktop/api/Winuser/nf-winuser-loadstringa) carica una risorsa di stringa dal file eseguibile di un'applicazione. La funzione [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) carica una risorsa di stringa e interpreta le opzioni di formattazione che possono essere incorporate nella stringa.

Le risorse in formato binario sono archiviate in formato Unicode. Quando si caricano risorse, le applicazioni possono usare la versione Unicode delle funzioni di risorsa (ad esempio,[**LoadStringW**](/windows/desktop/api/Winuser/nf-winuser-loadstringa)) per ottenere le risorse come dati Unicode.

Per le risorse di stringa a 16 bit, 255 caratteri è la lunghezza massima. Per le risorse di stringa a 32 bit, 65535 caratteri è la lunghezza massima.

 

 