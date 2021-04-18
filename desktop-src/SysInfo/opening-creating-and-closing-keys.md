---
description: Prima che un'applicazione possa aggiungere dati al registro di sistema, deve creare o aprire una chiave.
ms.assetid: 7b0b24d2-b54f-4243-95d0-2adbd87cb4df
title: Apertura, creazione e chiusura di chiavi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3260c255240ce2c7fb5d13fe28126a1a3f5527
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308097"
---
# <a name="opening-creating-and-closing-keys"></a>Apertura, creazione e chiusura di chiavi

Prima che un'applicazione possa aggiungere dati al registro di sistema, deve creare o aprire una chiave. Per creare o aprire una chiave, un'applicazione fa sempre riferimento alla chiave come sottochiave di una chiave attualmente aperta. Le seguenti chiavi predefinite sono sempre aperte: **HKEY \_ Local \_ computer**, **HKEY \_ Classes \_ root**, **HKEY \_ Users** e **HKEY \_ Current \_ User**. Un'applicazione usa la funzione [**RegOpenKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regopenkeyexa) per aprire una chiave e la funzione [**RegCreateKeyEx**](/windows/desktop/api/Winreg/nf-winreg-regcreatekeyexa) per creare una chiave. Un albero del registro di sistema può avere una profondità di 512 livelli. È possibile creare fino a 32 livelli alla volta tramite una singola chiamata API del registro di sistema.

Un'applicazione può usare la funzione [**RegCloseKey**](/windows/desktop/api/Winreg/nf-winreg-regclosekey) per chiudere una chiave e scrivere i dati in esso contenuti nel registro di sistema. **RegCloseKey** non scrive necessariamente i dati nel registro di sistema prima di restituire; il scaricamento della cache sul disco rigido può richiedere fino a pochi secondi. Se un'applicazione deve scrivere in modo esplicito i dati del registro di sistema sul disco rigido, può usare la funzione [**RegFlushKey ha**](/windows/desktop/api/Winreg/nf-winreg-regflushkey) . **RegFlushKey ha**, tuttavia, utilizza molte risorse di sistema e deve essere chiamato solo quando è strettamente necessario.

 

 



