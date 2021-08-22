---
description: Messaggi di errore della funzione del pacchetto del tipo di carattere
ms.assetid: 3cf7a8a1-66b2-45ca-b53d-29c80f95ff70
title: Messaggi di errore della funzione del pacchetto del tipo di carattere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7008707675d9b2ef3eb31229535b07b1af6000e43d1122c2929fd12988fb4ea3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118761084"
---
# <a name="font-package-function-error-messages"></a>Messaggi di errore della funzione del pacchetto del tipo di carattere

I valori LONG seguenti vengono restituiti dalle funzioni del pacchetto del tipo di carattere ( [**CreateFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-createfontpackage) e [**MergeFontPackage**](/windows/desktop/api/FontSub/nf-fontsub-mergefontpackage) ) quando vengono rilevati errori. Se le funzioni hanno esito positivo, viene restituito \_ il valore NO ERROR.



| Valore restituito                   | Valore | Descrizione                                                                                                      |
|--------------------------------|-------|------------------------------------------------------------------------------------------------------------------|
| NESSUN \_ ERRORE                      | 0     | Non si sono verificati errori.                                                                                               |
| FORMATO \_ ERR                    | 1006  | Si è verificato un errore di formato dei dati di input.                                                                             |
| ERR \_ GENERICO                   | 1000  | Si è verificato un errore nel codice generico.                                                                               |
| ERR \_ MEM                       | 1005  | Si è verificato un errore durante l'allocazione della memoria.                                                                      |
| ERR \_ NO \_ GLYPHS                | 1009  | Non sono stati trovati glifi.                                                                                            |
| BASE ERR \_ NON \_ VALIDA             | 1085  | Il tipo di carattere contiene una tabella di dati di base non valida. Attualmente questo valore non viene usato.                      |
| CMAP ERR \_ \_ NON VALIDO             | 1030  | Il tipo di carattere contiene una tabella di mapping da carattere a glifo (cmap) non valida.                                           |
| FORMATO DELTA \_ ERR \_ NON \_ VALIDO    | 1013  | È stato rilevato un formato delta non valido durante il tentativo di creare un subset di un tipo di carattere in formato 1 o 2.                                |
| ERR \_ \_ EBLC NON VALIDO             | 1086  | Il tipo di carattere contiene una tabella EBLC (Embedded Bitmap Location Data) non valida.                                        |
| ERR \_ INVALID \_ GLYF             | 1061  | Il tipo di carattere contiene una tabella di dati del glifo (glifo) non valida.                                                           |
| GDEF \_ ERR \_ NON VALIDO             | 1083  | Il tipo di carattere contiene una tabella GDEF (GLYPH Definition Data) non valida. Attualmente questo valore non viene usato.              |
| ERR \_ NON \_ VALIDO GPOS             | 1082  | Il tipo di carattere contiene una tabella GPOS (GPOS) di posizionamento del glifo non valida. Attualmente questo valore non viene usato.             |
| ERR \_ NON \_ VALIDO GSUB             | 1081  | Il tipo di carattere contiene una tabella GSUB (GLYPH Substitution Data) non valida.                                              |
| ERR \_ NON \_ VALIDO HDMX             | 1089  | Il tipo di carattere contiene una tabella hdmx (Horizontal Device Metrics) non valida.                                            |
| ERR \_ INVALID \_ HEAD             | 1062  | Il tipo di carattere contiene una tabella di intestazione (intestazione) del tipo di carattere non valida.                                                          |
| ERR \_ INVALID \_ HHEA             | 1063  | Il tipo di carattere contiene una tabella di intestazione orizzontale (hhea) non valida.                                                    |
| ERR \_ INVALID \_ HHEA \_ O \_ VHEA   | 1072  | Il tipo di carattere contiene una tabella di intestazione orizzontale (hhea) non valida o una tabella di intestazione delle metriche verticali (vhea) non valida. |
| ERR \_ INVALID \_ HMTX             | 1064  | Il tipo di carattere contiene una tabella delle metriche orizzontali (hmtx) non valida.                                                   |
| ERR \_ NON \_ VALIDO HMTX \_ O \_ VMTX   | 1073  | Il tipo di carattere contiene una tabella di metriche orizzontali (hmtx) non valida o una tabella di metriche verticali (vmtx) non valida.       |
| ERR \_ INVALID \_ JSTF             | 1084  | Il tipo di carattere contiene una tabella JSTF (Invalid Justification Data).                                                   |
| ERR \_ INVALID \_ LTSH             | 1087  | Il tipo di carattere contiene una tabella LTSH (Linear Threshold Data) non valida.                                                |
| ERR \_ INVALID \_ TTO              | 1080  | Tipo di carattere TrueType Open non valido.                                                                      |
| ERR \_ \_ VDMX NON VALIDO             | 1088  | Il tipo di carattere contiene una tabella VDMX (Vertical Device Metrics) non valida.                                              |
| ERR \_ INVALID \_ LOCA             | 1065  | Il tipo di carattere contiene un indice non valido nella tabella di posizione (loca).                                                    |
| ERR \_ INVALID \_ MAXP             | 1066  | Il tipo di carattere contiene una tabella di profilo massimo (maxp) non valida.                                                      |
| CHECKSUM \_ \_ DI MERGE NON VALIDI \_ ERR | 1011  | Tentativo di unione dei checksum per due tipi di carattere di un tipo di carattere padre diverso non riuscito.                       |
| FORMATI DI \_ MERGE ERR \_ NON \_ VALIDI   | 1010  | Tentativo di unione dei tipi di carattere con formati dttf non riusciti.                                          |
| \_ \_ NUMGLYPH MERGE \_ NON VALIDI ERR | 1012  | Il tentativo di unire il numero di glifi per due tipi di carattere di un tipo di carattere madre diverso non è riuscito.            |
| NOME ERR \_ NON \_ VALIDO             | 1067  | Il nome del pacchetto o il nome del tipo di carattere non è valido.                                                                |
| POST ERR \_ NON \_ VALIDO             | 1068  | Il tipo di carattere contiene una tabella PostScript di informazioni (post) non valida.                                               |
| ERR \_ INVALID \_ OS2              | 1069  | Il tipo di carattere contiene una tabella OS/2 e Windows specifica del sistema operativo(OS/2) non valida.                                    |
| ERR \_ INVALID \_ VHEA             | 1070  | Il tipo di carattere contiene una tabella di intestazione delle metriche verticali (vhea) non valida.                                              |
| ERR \_ INVALID \_ VMTX             | 1071  | Il tipo di carattere contiene una tabella di metriche verticali (vmtx) non valida.                                                     |
| INDICE \_ \_ TTC ERR NON \_ VALIDO       | 1015  | È stato passato un indice in base zero (TTC) non valido nel file del tipo di carattere.                                                 |
| ERR \_ MISSING \_ CMAP             | 1030  | Il tipo di carattere non contiene una tabella cmap.                                                                           |
| ERR \_ \_ MANCANTE IN EBDT             | 1044  | Il tipo di carattere non contiene una tabella EBDT.                                                                          |
| ERR \_ MISSING \_ GLYF             | 1031  | Il tipo di carattere non contiene una tabella glyf.                                                                           |
| ERR \_ MISSING \_ HEAD             | 1032  | Il tipo di carattere non contiene una tabella head.                                                                           |
| ERR \_ MISSING \_ HHEA             | 1033  | Il tipo di carattere non contiene una tabella hhea.                                                                          |
| ERR \_ \_ MANCANTE HMTX             | 1034  | Il tipo di carattere non contiene una tabella hmtx.                                                                          |
| ERR \_ MISSING \_ LOCA             | 1035  | Il tipo di carattere non contiene una tabella loca.                                                                           |
| ERR \_ MISSING \_ MAXP             | 1036  | Il tipo di carattere non contiene una tabella maxp.                                                                           |
| NOME \_ MANCANTE \_ ERR             | 1037  | Il tipo di carattere non contiene una tabella di denominazione (nome).                                                                  |
| POST \_ MANCANTE ERR \_             | 1038  | Il tipo di carattere non contiene una tabella post.                                                                           |
| ERR \_ MISSING \_ OS2              | 1039  | Il tipo di carattere non contiene una tabella del sistema operativo/2.                                                                          |
| ERR \_ MISSING \_ VHEA             | 1040  | Il tipo di carattere non contiene una tabella vhea.                                                                           |
| ERR \_ MISSING \_ VMTX             | 1041  | Il tipo di carattere non contiene una tabella vmtx.                                                                           |
| ERR \_ \_ MANCANTE HHEA \_ O \_ VHEA   | 1042  | Il tipo di carattere non contiene una tabella hhea o una tabella vhea.                                                          |
| ERR \_ \_ MANCANTE HMTX \_ O \_ VMTX   | 1043  | Il tipo di carattere non contiene una tabella hmtx o una tabella vmtx.                                                          |
| ERR \_ NON \_ TTC                  | 1014  | Il valore specificato non è un indice per un file TTC.                                                              |
| ERR \_ PARAMETER0                | 1100  | Il parametro 0 della funzione chiamante non è valido.                                                                        |
| ERR \_ PARAMETER1                | 1101  | La chiamata al parametro 1 della funzione non è valida.                                                                        |
| ERR \_ PARAMETER2                | 1102  | La chiamata al parametro 2 della funzione non è valida.                                                                        |
| PARAMETRO \_ ERR3                | 1103  | Il parametro 3 della funzione chiamante non è valido.                                                                        |
| ERR \_ PARAMETER4                | 1104  | Il parametro 4 della funzione chiamante non è valido.                                                                        |
| ERR \_ PARAMETER5                | 1105  | Il parametro 5 della funzione chiamante non è valido.                                                                        |
| PARAMETRO \_ ERR6                | 1106  | Il parametro 6 della funzione chiamante non è valido.                                                                        |
| ERR \_ PARAMETER7                | 1107  | La chiamata al parametro 7 della funzione non è valida.                                                                        |
| PARAMETRO \_ ERR8                | 1108  | Il parametro 8 della funzione chiamante non è valido.                                                                        |
| ERR \_ PARAMETER9                | 1109  | Il parametro 9 della funzione chiamante non è valido.                                                                        |
| PARAMETRO \_ ERR10               | 1110  | La chiamata al parametro 10 della funzione non è valida.                                                                       |
| PARAMETRO \_ ERR11               | 1111  | La chiamata al parametro della funzione 11 non è valida.                                                                       |
| PARAMETRO \_ ERR12               | 1112  | Il parametro 12 della funzione chiamante non è valido.                                                                       |
| PARAMETRO \_ ERR13               | 1113  | Il parametro 13 della funzione chiamante non è valido.                                                                       |
| PARAMETRO \_ ERR14               | 1114  | Il parametro 14 della funzione chiamante non è valido.                                                                       |
| PARAMETRO \_ ERR15               | 1115  | Il parametro 15 della funzione chiamante non è valido.                                                                       |
| PARAMETRO \_ ERR16               | 1116  | La chiamata al parametro della funzione 16 non è valida.                                                                       |
| ERR \_ READCONTROL               | 1003  | La struttura del controllo di lettura non corrisponde ai dati.                                                                   |
| ERR \_ READOUTOFBOUNDS           | 1001  | La lettura dalla memoria non è consentita, probabilmente perché i dati non erano in limiti o danneggiati.                          |
| VERSIONE \_ ERR                   | 1008  | Il valore dttf.version principale dei dati di input è maggiore della versione che la funzione può leggere.                   |
| ERR \_ AUMENTA \_               | 1007  | L'azione richiesta ha causato l'crescita dei dati e l'applicazione deve usare i dati originali.                             |
| ERR \_ WRITECONTROL              | 1004  | La struttura del controllo di scrittura non corrisponde ai dati.                                                                  |
| ERR \_ WRITEOUTOFBOUNDS          | 1002  | La scrittura in memoria non è consentita, probabilmente perché i dati non erano in limiti.                                      |



 

 

 



