---
description: Nel Windows a 64 bit, parti delle voci del Registro di sistema vengono archiviate separatamente per applicazioni a 32 bit e applicazioni a 64 bit e mappate in visualizzazioni del Registro di sistema logiche separate usando il redirector del Registro di sistema e la reflection del Registro di sistema, perché la versione a 64 bit di un'applicazione può usare chiavi e valori del Registro di sistema diversi rispetto alla versione a 32 bit. Sono inoltre presenti chiavi del Registro di sistema condivise che non vengono reindirizzate o riflesse.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Dati dell'applicazione a 32 bit e a 64 bit nel Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d87d5177eb48a5497e321b47bb0da96874a0e6522360f2dc519dc72df3dcdf89
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764985"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a>Dati dell'applicazione a 32 bit e a 64 bit nel Registro di sistema

Nel Windows a 64 bit, parti delle voci del Registro di sistema vengono archiviate separatamente per applicazioni a 32 bit e applicazioni a 64 bit e mappate in viste del Registro di sistema logiche separate usando il [redirector](/windows/desktop/WinProg64/registry-redirector) del Registro di sistema e la [reflection](/windows/desktop/WinProg64/registry-reflection)del Registro di sistema , perché la versione a 64 bit di un'applicazione può usare chiavi e valori del Registro di sistema diversi rispetto alla versione a 32 bit. Sono inoltre presenti [chiavi del Registro di](/windows/desktop/WinProg64/shared-registry-keys) sistema condivise che non vengono reindirizzate o riflesse.

L'elemento padre di ogni nodo del Registro di sistema a 64 bit è Image-Specific nodo o IS. Il redirector del Registro di sistema indirizza in modo trasparente l'accesso al Registro di sistema di un'applicazione al sottonodo ISN appropriato. I sottonodi di reindirizzamento nell'albero del Registro di sistema vengono creati automaticamente dal componente WOW64 usando il nome **Wow6432Node.** Di conseguenza, è essenziale non assegnare un nome ad alcuna chiave del Registro di sistema creata **in Wow6432Node.**

I flag KEY \_ WOW64 \_ 64KEY e KEY WOW64 32KEY consentono l'accesso esplicito rispettivamente alla visualizzazione del Registro di sistema a 64 bit e alla visualizzazione a \_ \_ 32 bit. Per altre informazioni, vedere [Accesso a una visualizzazione alternativa del Registro di sistema.](/windows/desktop/WinProg64/accessing-an-alternate-registry-view)

Per disabilitare e abilitare la reflection del Registro di sistema per una chiave specifica, usare le funzioni [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey.**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) Le applicazioni devono disabilitare la reflection solo per le chiavi del Registro di sistema create e non tentare di disabilitare la reflection per le chiavi predefinite, ad esempio **HKEY \_ LOCAL \_ MACHINE** o **HKEY \_ CURRENT \_ USER.** Per determinare le chiavi presenti nell'elenco di reflection, usare la [**funzione RegQueryReflectionKey.**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[redirector del Registro di sistema](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[reflection del Registro di sistema](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
