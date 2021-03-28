---
description: Messaggi di errore della funzione del pacchetto di tipi di carattere
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Messaggi di errore della funzione del pacchetto di tipi di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06bcf84f92b60351e8375df682de0c3b01c2aa1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130770"
---
# <a name="font-package-function-error-messages"></a>Messaggi di errore della funzione del pacchetto di tipi di carattere

I valori LONG seguenti vengono restituiti dalle funzioni del pacchetto di caratteri ( [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) e [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) ) quando vengono rilevati errori. Quando le funzioni hanno esito positivo, il valore non \_ viene restituito alcun errore.



| Valore restituito                   | Valore | Descrizione                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| Nessun \_ errore                      | 0     | Non si sono verificati errori.                                                                                               |
| \_formato Err                    | 1006  | Si è verificato un errore di formato dei dati di input.                                                                             |
| ERRORE \_ generico                   | 1000  | Si è verificato un errore nel codice generico.                                                                               |
| memoria \_ errore                       | 1005  | Si è verificato un errore durante l'allocazione della memoria.                                                                      |
| \_nessun \_ glifo                | 1009  | Non sono stati trovati glifi.                                                                                            |
| \_base Err non valida \_             | 1085  | Il tipo di carattere contiene una tabella dati Baseline (BASE) non valida. Attualmente questo valore non viene utilizzato.                      |
| ERRORE \_ CMap non valido \_             | 1030  | Il tipo di carattere contiene una tabella di mapping carattere a glifo (CMAP) non valida.                                           |
| \_ \_ formato Delta non \_ valido    | 1013  | È stato rilevato un formato Delta non valido durante il tentativo di sottoporre a subset un tipo di carattere di formato 1 o 2.                                |
| ERRORE \_ EBLC non valido \_             | 1086  | Il tipo di carattere contiene una tabella dati percorso bitmap incorporata (EBLC) non valida.                                        |
| ERRORE \_ GLYF non valido \_             | 1061  | Il tipo di carattere contiene una tabella dei dati di glifo (glyf) non valida.                                                           |
| ERRORE \_ GDEF non valido \_             | 1083  | Il tipo di carattere contiene una tabella dei dati di definizione di glifo (GDEF) non valida. Attualmente questo valore non viene utilizzato.              |
| ERRORE \_ oggetti Criteri di gruppo non validi \_             | 1082  | Il tipo di carattere contiene una tabella dei dati (GPO) del posizionamento del glifo non valida. Attualmente questo valore non viene utilizzato.             |
| ERRORE \_ gsub non valido \_             | 1081  | Il tipo di carattere contiene una tabella GSUB (Glyph Substitution Data) non valida.                                              |
| ERRORE \_ HDMX non valido \_             | 1089  | Il tipo di carattere contiene una tabella metrica del dispositivo orizzontale (HDMx) non valida.                                            |
| \_intestazione Err non valida \_             | 1062  | Il tipo di carattere contiene una tabella di intestazione del tipo di carattere (Head) non valida.                                                          |
| ERRORE \_ HHEA non valido \_             | 1063  | Il tipo di carattere contiene una tabella di intestazione orizzontale (hhea) non valida.                                                    |
| ERR \_ \_ HHEA \_ o \_ VHEA non valido   | 1072  | Il tipo di carattere contiene una tabella di intestazione orizzontale (hhea) non valida o una tabella vhea (Vertical Metrics header) non valida. |
| ERRORE \_ HMTX non valido \_             | 1064  | Il tipo di carattere contiene una tabella di metrica orizzontale (hmtx) non valida.                                                   |
| ERR \_ \_ HMTX \_ o \_ VMTX non valido   | 1073  | Il tipo di carattere contiene una tabella di metriche orizzontali (hmtx) non valida o una tabella di metriche verticali (vmtx) non valida.       |
| ERRORE \_ JSTF non valido \_             | 1084  | Il tipo di carattere contiene una tabella dei dati di giustificazione (JSTF) non valida.                                                   |
| ERRORE \_ LTSH non valido \_             | 1087  | Il tipo di carattere contiene una tabella dei dati di soglia lineare (LTSH) non valida.                                                |
| ERRORE \_ tto non valido \_              | 1080  | Il tipo di carattere è un tipo di carattere aperto TrueType non valido.                                                                      |
| ERRORE \_ VDMX non valido \_             | 1088  | Il tipo di carattere contiene una tabella metrica del dispositivo verticale (VDMX) non valida.                                              |
| ERRAta \_ Loca non valida \_             | 1065  | Il tipo di carattere contiene una tabella index (percorso) non valida.                                                    |
| ERRORE \_ MAXP non valido \_             | 1066  | Il tipo di carattere contiene una tabella MaxP (Maximum profile) non valida.                                                      |
| \_checksum di \_ merge non validi per ERR \_ | 1011  | Il tentativo di unire i checksum per due tipi di carattere da un tipo di carattere diverso da una madre non è riuscito.                       |
| \_formati di \_ merge non validi per ERR \_   | 1010  | Il tentativo di unire i tipi di carattere con formati DTTF non corretti non è riuscito.                                          |
| ERRORE \_ di \_ merge \_ NUMGLYPHS non valido | 1012  | Il tentativo di unire il numero di glifi per due tipi di carattere da un tipo di carattere diverso da una madre non è riuscito.            |
| ERRORE \_ nome non valido \_             | 1067  | Il nome del pacchetto di caratteri o il nome del tipo di carattere non è valido.                                                                |
| ERRORE \_ post non valido \_             | 1068  | Il tipo di carattere contiene una tabella di informazioni PostScript non valida (post).                                               |
| ERRORE \_ OS2 non valido \_              | 1069  | Il tipo di carattere contiene una tabella del sistema operativo/2 e delle metriche specifiche di Windows (OS/2).                                    |
| ERRORE \_ VHEA non valido \_             | 1070  | Il tipo di carattere contiene una tabella di intestazione di metrica verticale (vhea) non valida.                                              |
| ERRORE \_ VMTX non valido \_             | 1071  | Il tipo di carattere contiene una tabella di metrica verticale (vmtx) non valida.                                                     |
| ERRORE \_ dell' \_ Indice TTC non valido \_       | 1015  | È stato passato un indice in base zero (TTC) non valido nel file del tipo di carattere.                                                 |
| ERRORE \_ \_ CMap mancante             | 1030  | Il tipo di carattere non contiene una tabella CMAP.                                                                           |
| ERRORE \_ \_ EBDT mancante             | 1044  | Il tipo di carattere non contiene una tabella EBDT.                                                                          |
| ERRORE \_ \_ GLYF mancante             | 1031  | Il tipo di carattere non contiene una tabella glyf.                                                                           |
| \_intestazione mancante nel ERR \_             | 1032  | Il tipo di carattere non contiene una tabella Head.                                                                           |
| ERRORE \_ \_ HHEA mancante             | 1033  | Il tipo di carattere non contiene una tabella hhea.                                                                          |
| ERRORE \_ \_ HMTX mancante             | 1034  | Il tipo di carattere non contiene una tabella hmtx.                                                                          |
| ERR \_ mancante \_ loca             | 1035  | Il tipo di carattere non contiene una tabella loca.                                                                           |
| ERRORE \_ \_ MAXP mancante             | 1036  | Il tipo di carattere non contiene una tabella MaxP.                                                                           |
| \_nome mancante \_ Err             | 1037  | Il tipo di carattere non contiene una tabella di denominazione (nome).                                                                  |
| ERRORE \_ \_ post mancante             | 1038  | Il tipo di carattere non contiene una tabella post.                                                                           |
| ERRORE \_ \_ OS2 mancante              | 1039  | Il tipo di carattere non contiene una tabella OS/2.                                                                          |
| ERRORE \_ \_ VHEA mancante             | 1040  | Il tipo di carattere non contiene una tabella vhea.                                                                           |
| ERRORE \_ \_ VMTX mancante             | 1041  | Il tipo di carattere non contiene una tabella vmtx.                                                                           |
| ERR \_ mancante \_ HHEA \_ o \_ VHEA   | 1042  | Il tipo di carattere non contiene una tabella hhea o una tabella vhea.                                                          |
| ERR \_ mancante \_ HMTX \_ o \_ VMTX   | 1043  | Il tipo di carattere non contiene una tabella hmtx o una tabella vmtx.                                                          |
| ERR \_ non \_ TTC                  | 1014  | Il valore specificato non è un indice per un file TTC.                                                              |
| \_PARAMETER0 Err                | 1100  | Il parametro 0 della funzione chiamante non è valido.                                                                        |
| \_PARAMETRO1 Err                | 1101  | La chiamata al parametro 1 della funzione non è valida.                                                                        |
| \_PARAMETRO2 Err                | 1102  | Il parametro 2 della funzione chiamante non è valido.                                                                        |
| \_PARAMETRO3 Err                | 1103  | La chiamata al parametro 3 della funzione non è valida.                                                                        |
| \_PARAMETRO4 Err                | 1104  | La chiamata al parametro 4 della funzione non è valida.                                                                        |
| \_PARAMETER5 Err                | 1105  | Il parametro 5 della funzione chiamante non è valido.                                                                        |
| \_PARAMETER6 Err                | 1106  | La chiamata al parametro 6 della funzione non è valida.                                                                        |
| \_PARAMETER7 Err                | 1107  | Il parametro della funzione chiamante 7 non è valido.                                                                        |
| \_PARAMETER8 Err                | 1108  | Il parametro della funzione chiamante 8 non è valido.                                                                        |
| \_PARAMETER9 Err                | 1109  | Il parametro della funzione chiamante 9 non è valido.                                                                        |
| \_PARAMETER10 Err               | 1110  | Il parametro della funzione chiamante 10 non è valido.                                                                       |
| \_PARAMETER11 Err               | 1111  | Il parametro della funzione chiamante 11 non è valido.                                                                       |
| \_PARAMETER12 Err               | 1112  | La chiamata del parametro 12 della funzione non è valida.                                                                       |
| \_PARAMETER13 Err               | 1113  | Il parametro della funzione chiamante 13 non è valido.                                                                       |
| \_PARAMETER14 Err               | 1114  | Il parametro della funzione chiamante 14 non è valido.                                                                       |
| \_PARAMETER15 Err               | 1115  | Il parametro della funzione chiamante 15 non è valido.                                                                       |
| \_PARAMETER16 Err               | 1116  | Il parametro della funzione chiamante 16 non è valido.                                                                       |
| \_READCONTROL Err               | 1003  | La struttura del controllo Read non corrisponde ai dati.                                                                   |
| \_READOUTOFBOUNDS Err           | 1001  | Una lettura dalla memoria non è consentita, probabilmente perché i dati sono fuori limite o danneggiati.                          |
| \_versione Err                   | 1008  | Il valore DTTF. Version principale dei dati di input è maggiore della versione che la funzione può leggere.                   |
| il \_ Err \_ aumenta               | 1007  | L'azione richiesta ha causato la crescita dei dati e l'applicazione deve utilizzare i dati originali.                             |
| \_WRITECONTROL Err              | 1004  | La struttura del controllo di scrittura non corrisponde ai dati.                                                                  |
| \_WRITEOUTOFBOUNDS Err          | 1002  | Una scrittura in memoria non è consentita, probabilmente perché i dati sono fuori limite.                                      |



 

 

 



