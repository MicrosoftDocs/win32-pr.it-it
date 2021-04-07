---
description: Nelle finestre a 64 bit, le parti delle voci del registro di sistema vengono archiviate separatamente per le applicazioni a 32 bit e a 64 bit e sono mappate in visualizzazioni del registro di sistema logiche separate usando il redirector del registro di sistema e la reflection del registro di sistema, perché la versione a 64 bit di un'applicazione può usare chiavi e valori del registro di sistema diversi dalla versione a 32 Sono inoltre disponibili chiavi del registro di sistema condivise che non vengono reindirizzate o riflesse.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Dati dell'applicazione a 32 bit e a 64 bit nel registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882041"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>Dati dell'applicazione a 32 bit e a 64 bit nel registro di sistema

Nelle finestre a 64 bit, le parti delle voci del registro di sistema vengono archiviate separatamente per le applicazioni a 32 bit e a 64 bit e sono mappate in visualizzazioni del registro di sistema logiche separate usando il [redirector del registro di sistema](/windows/desktop/WinProg64/registry-redirector) e la [Reflection del registro](/windows/desktop/WinProg64/registry-reflection)di sistema, perché la versione a 64 bit di un'applicazione può usare chiavi e valori del registro di sistema diversi dalla versione a 32 Sono inoltre disponibili [chiavi del registro di sistema condivise](/windows/desktop/WinProg64/shared-registry-keys) che non vengono reindirizzate o riflesse.

L'elemento padre di ogni nodo del registro di sistema a 64 bit è il nodo Image-Specific o ISN. Il redirector del registro di sistema indirizza in modo trasparente l'accesso del registro di sistema di un'applicazione al sottonodo ISN appropriato. I sottonodi di reindirizzamento nell'albero del registro di sistema vengono creati automaticamente dal componente WOW64 usando il nome **Wow6432Node**. Di conseguenza, è essenziale non assegnare un nome alla chiave del registro di sistema creata **Wow6432Node**.

I \_ \_ flag 64KEY WOW64 32KEY e chiave \_ WOW64 \_ abilitano l'accesso esplicito alla visualizzazione del registro di sistema a 64 bit e rispettivamente alla visualizzazione a 32 bit. Per ulteriori informazioni, vedere [accesso a una visualizzazione del registro di sistema alternativa](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).

Per disabilitare e abilitare la reflection del registro di sistema per una chiave specifica, usare le funzioni [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) . Le applicazioni devono disabilitare la reflection solo per le chiavi del registro di sistema create e non tentare di disabilitare la reflection per le chiavi predefinite, ad esempio il **\_ \_ computer locale HKEY** o l' **\_ \_ utente corrente di HKEY**. Per determinare quali chiavi si trovano nell'elenco Reflection, usare la funzione [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[redirector del registro di sistema](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[Reflection del registro di sistema](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
