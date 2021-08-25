---
title: Accesso a una visualizzazione alternativa del Registro di sistema
description: Per impostazione predefinita, un'applicazione a 32 bit in esecuzione su WOW64 accede alla visualizzazione del Registro di sistema a 32 bit e un'applicazione a 64 bit accede alla visualizzazione del Registro di sistema a 64 bit.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- Visualizzazioni del Registro di sistema programmazione Windows a 64 bit
- WOW64 64-bit Windows programmazione , visualizzazioni del Registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1642de971a2342ab26114803689b8de21dd66194618a8db23f97170bc8da576a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119859081"
---
# <a name="accessing-an-alternate-registry-view"></a>Accesso a una visualizzazione alternativa del Registro di sistema

Per impostazione predefinita, un'applicazione a 32 bit in esecuzione su WOW64 accede alla visualizzazione del Registro di sistema a 32 bit e un'applicazione a 64 bit accede alla visualizzazione del Registro di sistema a 64 bit. I flag seguenti consentono alle applicazioni a 32 bit di accedere alle chiavi reindirizzate nella visualizzazione del Registro di sistema a 64 bit e alle applicazioni a 64 bit di accedere alle chiavi reindirizzate nella visualizzazione del Registro di sistema a 32 bit. Questi flag non hanno alcun effetto sulle chiavi del Registro di sistema condivise. Per altre informazioni, vedere [Chiavi del Registro di sistema interessate da WOW64.](shared-registry-keys.md)



| Nome del flag         | Valore  | Descrizione                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CHIAVE \_ WOW64 \_ 64KEY | 0x0100 | Accedere a una chiave a 64 bit da un'applicazione a 32 bit o a 64 bit.                                                                                                                                                                                   |
| CHIAVE \_ WOW64 \_ 32KEY | 0x0200 | Accedere a una chiave a 32 bit da un'applicazione a 32 bit o a 64 bit.<br/>**Windows 10 in ARM:** Si riferisce alla visualizzazione del Registro di sistema ARM a 32 bit per i processi ARM a 32 bit e alla visualizzazione del Registro di sistema x86 a 32 bit per i processi ARM64 a 32 bit x86 e a 64 bit. |



 

Questi flag possono essere specificati nel *parametro samDesired* delle funzioni del Registro di sistema seguenti:

-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegDeleteKeyEx**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**Regopenkeyex**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

È possibile \_ specificare KEY WOW64 \_ 32KEY o KEY \_ WOW64 \_ 64KEY. Se vengono specificati entrambi i flag, la funzione ha esito negativo con ERROR \_ INVALID \_ PARAMETER.

**Windows Server 2008, Windows Vista, Windows Server 2003 e Windows XP:** Se vengono specificati entrambi i flag, il comportamento della funzione non è definito.

La [**funzione RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) non può essere usata per accedere a una visualizzazione alternativa del Registro di sistema.

Di seguito sono riportate le procedure consigliate per l'accesso al Registro di sistema da un'applicazione:

-   Dopo che l'applicazione ha eseguito l'accesso a una visualizzazione alternativa del Registro di sistema usando uno dei flag , tutte le operazioni successive (creazione, eliminazione o apertura) sulle chiavi figlio del Registro di sistema devono usare in modo esplicito lo stesso flag. In caso contrario, può verificarsi un comportamento imprevisto.
-   Per enumerare accuratamente tutte le chiavi in entrambe le visualizzazioni, eseguire l'enumerazione in due passaggi. Il primo passaggio deve usare un handle aperto con uno dei flag e l'altro passaggio deve usare un handle aperto con l'altro flag.

> [!Note]  
> Le **chiavi Wow6432Node** **e WowAA32Node** sono riservate. Per motivi di compatibilità, le applicazioni non devono usare direttamente queste chiavi.

 

Per informazioni sull'accesso alla visualizzazione alternativa del Registro di sistema tramite WMI, vedere Richiesta di dati [WMI in una piattaforma a 64 bit.](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Redirector del Registro di sistema](registry-redirector.md)
</dt> <dt>

[Reflection del Registro di sistema](registry-reflection.md)
</dt> </dl>

 

