---
description: Prima che un'applicazione possa aggiungere dati al Registro di sistema, deve creare o aprire una chiave.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Apertura, creazione e chiusura di chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 605d53a00506122c6350abd7f06e9166ed487de98c7910a3b7c3a913978492f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117763963"
---
# <a name="opening-creating-and-closing-keys"></a>Apertura, creazione e chiusura di chiavi

Prima che un'applicazione possa aggiungere dati al Registro di sistema, deve creare o aprire una chiave. Per creare o aprire una chiave, un'applicazione fa sempre riferimento alla chiave come sottochiave di una chiave attualmente aperta. Le chiavi predefinite seguenti sono sempre aperte: **HKEY \_ LOCAL \_ MACHINE**, **HKEY \_ CLASSES \_ ROOT**, **HKEY \_ USERS** e **HKEY CURRENT \_ \_ USER**. Un'applicazione usa [**la funzione RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) per aprire una chiave e la [**funzione RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) per creare una chiave. Un albero del Registro di sistema può avere una profondità di 512 livelli. È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del registro.

Un'applicazione può usare [**la funzione RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) per chiudere una chiave e scrivere i dati in essa contenuti nel Registro di sistema. **RegCloseKey non** scrive necessariamente i dati nel Registro di sistema prima della restituzione. Lo scaricamento della cache sul disco rigido può richiedere fino a diversi secondi. Se un'applicazione deve scrivere in modo esplicito i dati del Registro di sistema nel disco rigido, può usare la [**funzione RegFlushKey.**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) **RegFlushKey,** tuttavia, usa molte risorse di sistema e deve essere chiamato solo quando assolutamente necessario.

 

 



