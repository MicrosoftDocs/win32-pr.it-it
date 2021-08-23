---
description: Elenca i requisiti applicati dagli strumenti di amministrazione del sistema di password complessa.
ms.assetid: a84f83b2-181b-4f65-82bd-bc7f0689aad3
title: Imposizione e protezione delle password Passfilt.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c3e34e77b15ca9797240ce5647aa58decf3efa05f04cd431b3d723b148bf406
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119004897"
---
# <a name="strong-password-enforcement-and-passfiltdll"></a>Imposizione e protezione delle password Passfilt.dll

L'imposizione di password complessa può essere abilitata tramite gli strumenti di amministrazione del sistema. Se i criteri di amministrazione del sistema sono abilitati, le password devono soddisfare i requisiti minimi seguenti quando vengono create o modificate:

-   Le password non possono contenere il valore samAccountName (Nome account) dell'utente o l'intero displayName (valore Full Name). Entrambi i controlli non supportano la distinzione tra maiuscole e minuscole.
-   SamAccountName viene controllato per intero solo per determinare se fa parte della password. Se samAccountName è di lunghezza inferiore a tre caratteri, questo controllo viene ignorato.
-   DisplayName viene analizzato per i delimitatori: virgole, punti, trattini o trattini, caratteri di sottolineatura, spazi, simboli di cancelletto e tabulazioni. Se viene trovato uno di questi delimitatori, displayName viene suddiviso e tutte le sezioni analizzate (token) vengono confermate come non incluse nella password. I token di meno di tre caratteri vengono ignorati e le sottostringhe dei token non vengono controllate. Ad esempio, il nome "Erin M. Hagens" è suddiviso in tre token: "Erin", "M" e "Hagens". Poiché il secondo token è lungo un solo carattere, viene ignorato. Pertanto, questo utente non potrebbe avere una password che include "erin" o "hagens" come sottostringa in qualsiasi punto della password.
-   Le password devono contenere caratteri di tre delle cinque categorie seguenti.



| Categorie di caratteri                                                                                                                                                      | Esempio                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------|
| Lettere maiuscole delle lingue europae (da A a Z, con segni diacritici, greco e cirillico)<br/>                                                     | A, B, C, Z<br/>                |
| Lettere minuscole delle lingue europaiche (da a a z, acuto, con segni diacritici, greco e cirillico)<br/>                                            | a, b, c, z<br/>                |
| Numeri in base 10 (da 0 a 9)<br/>                                                                                                                                   | 0, 1, 2, 9<br/>                |
| Caratteri non alfanumerici (caratteri speciali)<br/>                                                                                                               | $,!,%,^,() {} \[ \] ;:<>?<br/> |
| Qualsiasi carattere Unicode categorizzato come carattere alfabetico ma non maiuscolo o minuscolo. Sono inclusi i caratteri Unicode delle lingue dell'Asia.<br/> |                                        |



 

**Per abilitare l'imposizione di password complessa**

1.  Dalla console di amministrazione individuare **Criteri di sicurezza locali**.
2.  Selezionare **Criteri account** e quindi Criteri **password.**
3.  Abilitare **l'impostazione Le password devono soddisfare i requisiti di** complessità.

> [!Note]  
> Un determinato carattere può soddisfare una sola categoria. La [funzione GetStringTypeW](/windows/win32/api/stringapiset/nf-stringapiset-getstringtypew) viene usata per verificare se ogni carattere nella password è maiuscolo, minuscolo o alfanumerico.

 

 

