---
description: Il Component Object Model (COM) è uno standard binario per la scrittura di software componente in un ambiente di elaborazione distribuito.
ms.assetid: 5a282158-63b0-4c15-9bfc-0d61f5fe8716
title: Backup e ripristino del database di registrazione della classe COM+ in VSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae21489330693f0ce0d23b8639507121b9b00302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318913"
---
# <a name="backing-up-and-restoring-the-com-class-registration-database-under-vss"></a>Backup e ripristino del database di registrazione della classe COM+ in VSS

Il Component Object Model (COM) è uno standard binario per la scrittura di software componente in un ambiente di elaborazione distribuito.

Gli identificatori dei componenti archiviati (GUID) dell'implementazione Win32 originale e altri Stati COM nel registro di sistema in **HKEY \_ classi \_ radice \\ CLSID**.

La generazione corrente del Component Object Model, COM+, offre un database indipendente dal registro di sistema per l'archiviazione delle informazioni di registrazione dei componenti, ovvero il database di registrazione della classe COM+.

Il database di registrazione della classe COM+ supporta una VSS writer, che consente ai richiedenti di eseguire il backup del database di registrazione usando i dati archiviati in un volume copiato in Shadow.

Per ripristinare il database di registrazione COM+, un richiedente deve chiamare il metodo [ICOMAdminCatalog:: RestoreREGDB](/windows/win32/api/comadmin/nf-comadmin-icomadmincatalog-restoreregdb) .

Per ulteriori informazioni sul writer del database di registrazione COM+, vedere la pagina relativa ai [writer VSS](in-box-vss-writers.md).

 

 
