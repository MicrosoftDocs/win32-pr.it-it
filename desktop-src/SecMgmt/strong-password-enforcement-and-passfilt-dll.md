---
description: Elenca i requisiti applicati da strumenti di amministrazione del sistema con password complesse.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Imposizione avanzata delle password e Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b7be524511d52048e06ae83ab110384c3bf5c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525705"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a>Imposizione avanzata delle password e Passfilt.dll

L'imposizione di password complesse può essere abilitata usando gli strumenti di amministrazione del sistema. Se il criterio di amministrazione del sistema è abilitato, le password devono soddisfare i requisiti minimi seguenti quando vengono create o modificate:

-   Le password non possono contenere il valore samAccountName (nome account) dell'utente o l'intero displayName (valore nome completo). I controlli non fanno distinzione tra maiuscole e minuscole.
-   L'oggetto samAccountName viene archiviato integralmente solo per determinare se fa parte della password. Se samAccountName è inferiore a tre caratteri, questo controllo viene ignorato.
-   Il displayName viene analizzato per i delimitatori: virgole, punti, trattini o trattini, caratteri di sottolineatura, spazi, segni di cancelletto e tabulazioni. Se uno di questi delimitatori viene trovato, displayName viene suddiviso e tutte le sezioni analizzate (token) vengono confermate per non essere incluse nella password. I token che sono meno di tre caratteri vengono ignorati e le sottostringhe dei token non vengono controllate. Il nome "Erin M. Hagens", ad esempio, è suddiviso in tre token: "Erin", "M" e "Hagens". Poiché il secondo token è lungo un solo carattere, viene ignorato. Pertanto, l'utente non può disporre di una password che includa "Erin" o "Hagens" come una sottostringa in un punto qualsiasi della password.
-   Le password devono contenere caratteri di tre delle cinque categorie riportate di seguito.



| Categorie di caratteri                                                                                                                                                      | Esempio                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Lettere maiuscole delle lingue europee (dalla A alla Z con segni diacritici, caratteri greci e cirillici)<br/>                                                     | A, B, C, Z<br/>                |
| Lettere minuscole delle lingue europee (da a a z, Sharp-s, con segni diacritici, caratteri greci e cirillici)<br/>                                            | a, b, c, z<br/>                |
| Numeri in base 10 (da 0 a 9)<br/>                                                                                                                                   | 0, 1, 2, 9<br/>                |
| Caratteri non alfanumerici (caratteri speciali)<br/>                                                                                                               | $,!,%, ^, () {} \[ \] ;: <>?<br/> |
| Qualsiasi carattere Unicode categorizzato come carattere alfabetico ma non è maiuscolo o minuscolo. Sono inclusi i caratteri Unicode delle lingue asiatiche.<br/> |                                        |



 

**Per abilitare l'applicazione di password complesse**

1.  Nella console di amministrazione individuare **criteri di sicurezza locali**.
2.  Selezionare **criteri account**, quindi selezionare **criteri password**.
3.  Abilitare le **password devono soddisfare i requisiti di complessità** impostazione.

> [!Note]  
> Un determinato carattere può soddisfare solo una categoria. La funzione [GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) viene utilizzata per verificare se ogni carattere della password è maiuscolo, minuscolo o alfanumerico.

 

 

