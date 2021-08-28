---
title: Stringhe
description: In questa sezione vengono illustrate le funzioni per le stringhe.
ms.assetid: vs|winui|~\winui\windowsuserinterface\resources\strings.htm
keywords:
- risorse, stringhe
- stringhe
- funzioni per i valori stringa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3799c151b828dba1d687068da6f7f5924aded09
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478897"
---
# <a name="strings"></a>Stringhe

In questa sezione vengono descritte le funzioni stringa e viene illustrato come usarle nelle applicazioni.

### <a name="in-this-section"></a>Contenuto della sezione



| Nome                                     | Descrizione                                             |
|------------------------------------------|---------------------------------------------------------|
| [Informazioni sulle stringhe](about-strings.md)       | Vengono illustrate le funzioni per le stringhe.<br/>              |
| [Informazioni su Strsafe.h](strsafe-ovw.md)       | Vengono illustrate le funzioni stringa in Strsafe.h.<br/> |
| [Informazioni di riferimento sulla stringa](string-reference.md) | Contiene il riferimento all'API.<br/>                  |



 

### <a name="string-functions"></a>Funzioni di stringa




| Nome | Descrizione | 
|------|-------------|
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowera"><strong>CharLower</strong></a> | Converte una stringa di caratteri o un singolo carattere in minuscolo. Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charlowerbuffa"><strong>CharLowerBuff</strong></a> | Converte i caratteri maiuscoli in un buffer in caratteri minuscoli. La funzione converte i caratteri sul posto. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnexta"><strong>CharNext</strong></a> | Recupera un puntatore al carattere successivo in una stringa. Questa funzione può gestire stringhe costituite da caratteri a uno o più byte.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charnextexa"><strong>CharNextExA</strong></a> | Recupera il puntatore al carattere successivo in una stringa. Questa funzione può gestire stringhe costituite da caratteri a uno o più byte.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charpreva"><strong>CharPrev</strong></a> | Recupera un puntatore al carattere precedente in una stringa. Questa funzione può gestire stringhe costituite da caratteri a uno o più byte.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charprevexa"><strong>CharPrevExA</strong></a> | Recupera il puntatore al carattere precedente in una stringa. Questa funzione può gestire stringhe costituite da caratteri a uno o più byte.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooema"><strong>CharToOem</strong></a> | Converte una stringa nel set di caratteri definito dall'OEM.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-chartooembuffa"><strong>CharToOemBuff</strong></a> | Converte un numero specificato di caratteri in una stringa nel set di caratteri definito dall'OEM.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charuppera"><strong>CharUpper</strong></a> | Converte una stringa di caratteri o un singolo carattere in maiuscolo. Se l'operando è una stringa di caratteri, la funzione converte i caratteri sul posto. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-charupperbuffa"><strong>CharUpperBuff</strong></a> | Converte i caratteri minuscoli in un buffer in caratteri maiuscoli. La funzione converte i caratteri sul posto. <br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a> | Confronta due stringhe di caratteri, usando le impostazioni locali specificate.<blockquote>[!Note]<br />Per la compatibilità con Unicode, <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>usare CompareStringEx</strong></a> o la versione Unicode di <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringw"><strong>CompareString</strong></a>.</blockquote><br /><br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-comparestringex"><strong>CompareStringEx</strong></a> | Confronta due stringhe Unicode (caratteri wide), usando le impostazioni locali specificate.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-foldstringw"><strong>FoldString</strong></a> | Mappe una stringa a un'altra, eseguendo un'opzione di trasformazione specificata. <br /> | 
| <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> | Recupera informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata. Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output. Ogni bit identifica un determinato tipo di carattere, ad esempio se il carattere è una lettera, una cifra o nessuno dei due.<br /> | 
| <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> | Recupera informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata. Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output. Ogni bit identifica un determinato tipo di carattere, ad esempio se il carattere è una lettera, una cifra o nessuno dei due. <br /> A differenza dei relativi vicini <a href="/windows/desktop/api/winnls/nf-winnls-getstringtypea"><strong>GetStringTypeA</strong></a> e <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW,</strong></a> <a href="/windows/win32/api/stringapiset/nf-stringapiset-getstringtypeexw"><strong>GetStringTypeEx</strong></a> presenta un comportamento standard tramite l'uso <strong>#define'opzione UNICODE.</strong> È la funzione consigliata.<br /> | 
| <a href="/windows/desktop/api/stringapiset/nf-stringapiset-getstringtypew"><strong>GetStringTypeW</strong></a> | Recupera informazioni sul tipo di carattere per i caratteri nella stringa di origine specificata. Per ogni carattere nella stringa, la funzione imposta uno o più bit nell'elemento a 16 bit corrispondente della matrice di output. Ogni bit identifica un determinato tipo di carattere, ad esempio se il carattere è una lettera, una cifra o nessuno dei due.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphaa"><strong>IsCharAlpha</strong></a> | Determina se un carattere è un carattere alfabetico. Questa determinazione si basa sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite Pannello di controllo. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaralphanumerica"><strong>IsCharAlphaNumeric</strong></a> | Determina se un carattere è alfabetico o numerico. Questa determinazione si basa sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite Pannello di controllo. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischarlowera"><strong>IsCharLower</strong></a> | Determina se un carattere è minuscolo. Questa determinazione si basa sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite Pannello di controllo. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-ischaruppera"><strong>IsCharUpper</strong></a> | Determina se un carattere è maiuscolo. Questa determinazione si basa sulla semantica della lingua selezionata dall'utente durante l'installazione o tramite Pannello di controllo. <br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-loadstringa"><strong>LoadString</strong></a> | Carica una risorsa stringa dal file eseguibile associato a un modulo specificato, copia la stringa in un buffer e aggiunge un carattere NULL di terminazione.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcata"><strong>lstrcat</strong></a> | Aggiunge una stringa a un'altra.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpa"><strong>lstrcmp</strong></a> | Confronta due stringhe di caratteri. Il confronto fa distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcmpia"><strong>lstrcmpi</strong></a> | Confronta due stringhe di caratteri. Nel confronto non viene fatta distinzione tra maiuscole e minuscole.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpya"><strong>lstrcpy</strong></a> | Copia una stringa in un buffer.<br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrcpyna"><strong>lstrcpyn</strong></a> | Copia un numero specificato di caratteri da una stringa di origine in un buffer. <br /> | 
| <a href="/windows/desktop/api/Winbase/nf-winbase-lstrlena"><strong>lstrlen</strong></a> | Determina la lunghezza della stringa specificata (senza includere il carattere Null di terminazione).<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtochara"><strong>OemToChar</strong></a> | Converte una stringa dal set di caratteri definito dall'OEM in una stringa ANSI o di caratteri wide.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-oemtocharbuffa"><strong>OemToCharBuff</strong></a> | Converte un numero specificato di caratteri in una stringa dal set di caratteri definito dall'OEM in una stringa di caratteri ANSI o wide.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wsprintfa"><strong>wsprintf</strong></a> | Scrive i dati formattati nel buffer specificato.<br /> | 
| <a href="/windows/desktop/api/Winuser/nf-winuser-wvsprintfa"><strong>wvsprintf</strong></a> | Scrive dati formattati nel buffer specificato usando un puntatore a un elenco di argomenti.<br /> | 




 

### <a name="strsafe-functions"></a>Funzioni Strsafe



| Nome                                             | Descrizione                                                                                      |
|--------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [**StringCbCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcata)               | Concatena una stringa a un'altra.<br/>                                            |
| [**StringCbCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatexa)           | Concatena una stringa a un'altra.<br/>                                            |
| [**StringCbCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatna)             | Concatena il numero specificato di byte da una stringa a un'altra.<br/>         |
| [**StringCbCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcatnexa)         | Concatena il numero specificato di byte da una stringa a un'altra.<br/>         |
| [**StringCbCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopya)             | Copia una stringa in un'altra.<br/>                                                         |
| [**StringCbCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyexa)         | Copia una stringa in un'altra.<br/>                                                         |
| [**StringCbCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopyna)           | Copia il numero specificato di byte da una stringa a un'altra.<br/>                      |
| [**StringCbCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbcopynexa)       | Copia il numero specificato di byte da una stringa a un'altra.<br/>                      |
| [**StringCbGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsa)             | Ottiene una riga di testo da stdin, fino al carattere di nuova riga (' \\ n').<br/>  |
| [**StringCbGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbgetsexa)         | Ottiene una riga di testo da stdin, fino al carattere di nuova riga (' \\ n').<br/>  |
| [**StringCbLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcblengtha)         | Determina se una stringa supera la lunghezza specificata, in byte.<br/>                   |
| [**StringCbPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfa)         | Scrive i dati formattati nella stringa specificata.<br/>                                        |
| [**StringCbPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbprintfexa)     | Scrive i dati formattati nella stringa specificata.<br/>                                        |
| [**StringCbVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfa)       | Scrive dati formattati nella stringa specificata usando un puntatore a un elenco di argomenti.<br/> |
| [**StringCbVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcbvprintfexa)   | Scrive dati formattati nella stringa specificata usando un puntatore a un elenco di argomenti.<br/> |
| [**StringCchCat**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcata)             | Concatena una stringa a un'altra.<br/>                                            |
| [**StringCchCatEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatexa)         | Concatena una stringa a un'altra.<br/>                                            |
| [**StringCchCatN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatna)           | Concatena il numero specificato di caratteri da una stringa a un'altra.<br/>    |
| [**StringCchCatNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcatnexa)       | Concatena il numero specificato di caratteri da una stringa a un'altra.<br/>    |
| [**StringCchCopy**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopya)           | Copia una stringa in un'altra.<br/>                                                         |
| [**StringCchCopyEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyexa)       | Copia una stringa in un'altra.<br/>                                                         |
| [**StringCchCopyN**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopyna)         | Copia il numero specificato di caratteri da una stringa a un'altra.<br/>                 |
| [**StringCchCopyNEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchcopynexa)     | Copia il numero specificato di caratteri da una stringa a un'altra.<br/>                 |
| [**StringCchGets**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsa)           | Ottiene una riga di testo da stdin, fino al carattere di nuova riga (' \\ n').<br/>  |
| [**StringCchGetsEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchgetsexa)       | Ottiene una riga di testo da stdin, fino al carattere di nuova riga (' \\ n').<br/>  |
| [**StringCchLength**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchlengtha)       | Determina se una stringa supera la lunghezza specificata, in caratteri.<br/>              |
| [**StringCchPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfa)       | Scrive i dati formattati nella stringa specificata.<br/>                                        |
| [**StringCchPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchprintfexa)   | Scrive i dati formattati nella stringa specificata.<br/>                                        |
| [**StringCchVPrintf**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfa)     | Scrive dati formattati nella stringa specificata usando un puntatore a un elenco di argomenti.<br/> |
| [**StringCchVPrintfEx**](/windows/desktop/api/Strsafe/nf-strsafe-stringcchvprintfexa) | Scrive dati formattati nella stringa specificata usando un puntatore a un elenco di argomenti.<br/> |



 

 

