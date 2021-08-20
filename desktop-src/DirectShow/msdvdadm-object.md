---
description: Oggetto MSDVDAdm
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: Oggetto MSDVDAdm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa4001def80bff94920996dc627869ffecfd6dda3fbc679be79f2b321ac33a1b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119072975"
---
# <a name="msdvdadm-object"></a>Oggetto MSDVDAdm

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

> [!Note]  
> Questa API è deprecata. Per informazioni sulla riproduzione e la navigazione dei DVD in DirectShow, vedere [DVD Applications](dvd-applications.md).

 

I metodi e le proprietà dell'oggetto "administration" consentono a un'applicazione di scripting di modificare le impostazioni predefinite nel `MSDVDAdm` Registro ® Windows® Microsoft. Il Registro di sistema è un database in tutti i Windows in cui le applicazioni possono archiviare informazioni su se stesse da usare durante l'inizializzazione o in fase di esecuzione.

La maggior parte di questi metodi e proprietà non imposta né recupera i valori correnti [nell'oggetto MSWebDVD](mswebdvd-object.md) stesso. Ciò significa, ad esempio, che quando si chiama **GetParentalLevel** il valore restituito non è il livello di genitori corrente archiviato nell'oggetto . Si tratta invece del livello di genitori predefinito archiviato nel registro. Per ottenere il livello di genitori corrente, chiamare il **metodo MSWebDVD** [**GetPlayerParentalLevel.**](getplayerparentallevel-method.md) La [**chiamata a SaveParentalLevel**](saveparentallevel-method.md) scrive semplicemente un nuovo livello di accesso dei genitori predefinito nel Registro di sistema. È comunque necessario chiamare il **metodo MSWebDVD** [**SelectParentalLevel**](selectparentallevel-method.md) per rendere immediatamente effettiva la modifica nell'oggetto **MSWebDVD.** I metodi dell'identificatore delle impostazioni locali (LCID) predefiniti funzionano in modo analogo.

D'altra parte, i metodi [**BookmarkOnStop**](bookmarkonstop-property.md) e [**BookmarkOnClose**](bookmarkonclose-property.md) hanno effetto immediato perché l'oggetto **MSWebDVD** controlla queste impostazioni appena prima che l'utente arresti la riproduzione o chiuda l'applicazione, anziché durante l'inizializzazione.

È possibile accedere `MSDVDAdm` all'oggetto **tramite la proprietà DVDAdm** **di MSWebDVD.** Ad esempio, se **l'oggetto MSWebDVD** è denominato "DVD", chiamare **ChangePassword** come illustrato nell'esempio di codice seguente.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Metodi e proprietà**

Nella tabella seguente sono elencati i metodi e le proprietà esposti dalle proprietà e dai metodi dell'oggetto MSDVDAdm.



| Metodo                                                          | Descrizione                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Salva una nuova password dell'applicazione nel Registro di sistema.                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | Salva un nuovo livello di genitori predefinito nel registro.                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | Salva il nuovo paese/area genitori dell'applicazione nel registro.                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | Verifica se la password specificata corrisponde alla password salvata in precedenza.                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | Recupera l'ultimo livello di genitori salvato nel registro.                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | Recupera l'ultimo paese/area genitori salvato nel registro.                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | Ripristina le impostazioni di screen saver sistema.                                                                                                                                       |
| Proprietà                                                        | Descrizione                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | Attiva o disattiva screen saver sistema.                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | Imposta o recupera l'impostazione del Registro di sistema per l'LCID predefinito specificato dall'utente per il flusso audio.                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | Imposta o recupera l'impostazione del Registro di sistema per l'LCID predefinito specificato dall'utente per il flusso dell'immagine secondaria.                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | Imposta o recupera l'impostazione del Registro di sistema per l'LCID predefinito specificato dall'utente per i menu.                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | Imposta o recupera un valore che indica all'oggetto MSDVDAdm se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente fa clic sul **pulsante** Arresta. |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | Imposta o recupera un valore che indica all'oggetto MSDVDAdm se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente chiude l'applicazione.     |



 

 

 



