---
description: Oggetto MSDVDAdm
ms.assetid: 753d2820-4d47-4e07-9f54-9b996e55f0b6
title: Oggetto MSDVDAdm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 193d5e46837c576c61b8bf1704ec967c1b6fc246
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104123474"
---
# <a name="msdvdadm-object"></a>Oggetto MSDVDAdm

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

> [!Note]  
> Questa API è deprecata. Per informazioni sulla riproduzione e l'esplorazione dei DVD in DirectShow, vedere [applicazioni DVD](dvd-applications.md).

 

I metodi e le proprietà dell' `MSDVDAdm` oggetto "Administration" consentono a un'applicazione di scripting di modificare le impostazioni predefinite nel registro di sistema di Microsoft® Windows®. Il registro di sistema è un database in tutti i sistemi Windows in cui le applicazioni possono archiviare le informazioni relative a se stesse per essere usate durante l'inizializzazione o in fase di esecuzione.

La maggior parte di questi metodi e proprietà non imposta o recupera i valori correnti nell'oggetto [mswebdvd](mswebdvd-object.md) . Ciò significa, ad esempio, che quando si chiama **GetParentalLevel** , il valore restituito non è il livello padre corrente archiviato nell'oggetto. È invece il livello padre predefinito archiviato nel registro di sistema. Per ottenere il livello padre corrente, chiamare il metodo **mswebdvd** [**GetPlayerParentalLevel**](getplayerparentallevel-method.md). La chiamata di [**SaveParentalLevel**](saveparentallevel-method.md) scrive semplicemente un nuovo livello di accesso padre predefinito nel registro di sistema; è comunque necessario chiamare il metodo **mswebdvd** [**SelectParentalLevel**](selectparentallevel-method.md) per rendere effettiva la modifica immediatamente nell'oggetto **mswebdvd** . I metodi predefiniti dell'identificatore delle impostazioni locali (LCID) funzionano in modo analogo.

D'altra parte, i metodi [**BookmarkOnStop**](bookmarkonstop-property.md) e [**BookmarkOnClose**](bookmarkonclose-property.md) diventano immediatamente effettivi perché l'oggetto **mswebdvd** controlla queste impostazioni poco prima che l'utente interrompa la riproduzione o chiude l'applicazione, anziché durante l'inizializzazione.

Si accede all' `MSDVDAdm` oggetto tramite la proprietà **DVDAdm** di **mswebdvd**. Se, ad esempio, l'oggetto **mswebdvd** è denominato "DVD", chiamare **ChangePassword** come illustrato nell'esempio di codice seguente.


```C++
DVD.DVDAdm.ChangePassword(sUserName, sOld, sNew)
```



**Metodi e proprietà**

Nella tabella seguente sono elencati i metodi e le proprietà esposti dai metodi e dalle proprietà dell'oggetto MSDVDAdm.



| Metodo                                                          | Descrizione                                                                                                                                                                      |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ChangePassword**](changepassword-method.md)                 | Salva una nuova password dell'applicazione nel registro di sistema.                                                                                                                                |
| [**SaveParentalLevel**](saveparentallevel-method.md)           | Salva un nuovo livello padre predefinito nel registro di sistema.                                                                                                                              |
| [**SaveParentalCountry**](saveparentalcountry-method.md)       | Salva il nuovo paese/area padre dell'applicazione nel registro di sistema.                                                                                                             |
| [**ConfirmPassword**](confirmpassword-method.md)               | Verifica se la password specificata corrisponde alla password salvata in precedenza.                                                                                                      |
| [**GetParentalLevel**](getparentallevel-method.md)             | Recupera il livello padre che è stato salvato per ultimo nel registro di sistema.                                                                                                                |
| [**GetParentalCountry**](getparentalcountry-method.md)         | Recupera il paese padre/area che è stato salvato per ultimo nel registro di sistema.                                                                                                       |
| [**RestoreScreenSaver**](restorescreensaver-method.md)         | Ripristina le impostazioni del screen saver di sistema.                                                                                                                                       |
| Proprietà                                                        | Descrizione                                                                                                                                                                      |
| [**DisableScreenSaver**](disablescreensaver-property.md)       | Attiva o disattiva la screen saver di sistema.                                                                                                                                         |
| [**DefaultAudioLCID**](defaultaudiolcid-property.md)           | Imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso audio.                                                                                 |
| [**DefaultSubpictureLCID**](defaultsubpicturelcid-property.md) | Imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per il flusso dell'immagine.                                                                            |
| [**DefaultMenuLCID**](defaultmenulcid-property.md)             | Imposta o recupera l'impostazione del registro di sistema per l'LCID predefinito specificato dall'utente per i menu.                                                                                            |
| [**BookmarkOnStop**](bookmarkonstop-property.md)               | Imposta o recupera un valore che indica all'oggetto MSDVDAdm se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente fa clic sul pulsante **Interrompi** . |
| [**BookmarkOnClose**](bookmarkonclose-property.md)             | Imposta o recupera un valore che indica all'oggetto MSDVDAdm se salvare automaticamente un segnalibro della posizione e delle impostazioni correnti quando l'utente chiude l'applicazione.     |



 

 

 



