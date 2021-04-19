---
title: Accesso a una visualizzazione del registro di sistema alternativa
description: Per impostazione predefinita, un'applicazione a 32 bit in esecuzione su WOW64 accede alla visualizzazione del Registro di sistema a 32 bit e un'applicazione a 64 bit accede alla visualizzazione del Registro di sistema a 64 bit.
ms.assetid: 2c5fd3de-998c-44ab-863e-8e0e90d56e5d
keywords:
- Visualizzazioni del registro di sistema a 64 bit programmazione Windows
- Programmazione Windows WOW64 a 64 bit, viste del registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad3bca57367394e1b2fffc6486065e93c966f224
ms.sourcegitcommit: 35bb565804eaeed7ac5503595753f59d120076dd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/09/2021
ms.locfileid: "106320252"
---
# <a name="accessing-an-alternate-registry-view"></a>Accesso a una visualizzazione del registro di sistema alternativa

Per impostazione predefinita, un'applicazione a 32 bit in esecuzione su WOW64 accede alla visualizzazione del Registro di sistema a 32 bit e un'applicazione a 64 bit accede alla visualizzazione del Registro di sistema a 64 bit. I flag seguenti consentono alle applicazioni a 32 bit di accedere alle chiavi reindirizzate nella visualizzazione del registro di sistema a 64 bit e alle applicazioni a 64 bit per accedere alle chiavi reindirizzate nella visualizzazione del registro di sistema a 32 bit. Questi flag non hanno effetto sulle chiavi del registro di sistema condivise. Per altre informazioni, vedere [chiavi del registro di sistema interessate da WOW64](shared-registry-keys.md).



| Nome del flag         | Valore  | Descrizione                                                                                                                                                                                                                                       |
|-------------------|--------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CHIAVE \_ WOW64 \_ 64KEY | 0x0100 | Accedere a una chiave a 64 bit da un'applicazione a 32 bit o a 64 bit.                                                                                                                                                                                   |
| CHIAVE \_ WOW64 \_ 32KEY | 0x0200 | Accedere a una chiave a 32 bit da un'applicazione a 32 bit o a 64 bit.<br/>**Windows 10 su ARM:** Si fa riferimento alla visualizzazione del registro di sistema ARM a 32 bit per i processi ARM a 32 bit e alla visualizzazione del registro di sistema x86 a 32 bit per i processi ARM64 a 32 bit x86 e a 64 bit. |



 

Questi flag possono essere specificati nel parametro *samDesired* delle funzioni del registro di sistema seguenti:

-   [**RegCreateKeyEx**](/windows/desktop/api/winreg/nf-winreg-regcreatekeyexa)
-   [**RegDeleteKeyEx**](/windows/desktop/api/winreg/nf-winreg-regdeletekeyexa)
-   [**RegOpenKeyEx**](/windows/desktop/api/winreg/nf-winreg-regopenkeyexa)

\_ \_ È possibile specificare la chiave WOW64 32KEY o la chiave \_ WOW64 \_ 64KEY. Se vengono specificati entrambi i flag, la funzione ha esito negativo con errore \_ parametro non valido \_ .

**Windows server 2008, Windows Vista, Windows server 2003 e Windows XP:** Se vengono specificati entrambi i flag, il comportamento della funzione non è definito.

Impossibile utilizzare la funzione [**RegDeleteKey**](/windows/desktop/api/winreg/nf-winreg-regdeletekeya) per accedere a una visualizzazione del registro di sistema alternativa.

Di seguito sono illustrate le procedure consigliate per l'accesso al registro di sistema da un'applicazione:

-   Dopo che l'applicazione ha eseguito l'accesso a una visualizzazione del registro di sistema alternativa utilizzando uno dei flag, tutte le operazioni successive (crea, Elimina o Apri) sulle chiavi del registro di sistema figlio devono utilizzare in modo esplicito lo stesso flag. In caso contrario, è possibile che si verifichi un comportamento imprevisto.
-   Per enumerare accuratamente tutte le chiavi in entrambe le visualizzazioni, eseguire l'enumerazione in due passaggi. Il primo passaggio deve usare un handle aperto con uno dei flag e l'altro pass deve usare un handle aperto con l'altro flag.

> [!Note]  
> Le chiavi **Wow6432Node** e **WowAA32Node** sono riservate. Per compatibilità, le applicazioni non devono utilizzare direttamente queste chiavi.

 

Per informazioni sull'accesso alla visualizzazione del registro di sistema alternativa tramite WMI, vedere [richiesta di dati WMI in una piattaforma a 64 bit](/windows/desktop/WmiSdk/requesting-wmi-data-on-a-64-bit-platform).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Redirector del registro di sistema](registry-redirector.md)
</dt> <dt>

[Reflection del registro di sistema](registry-reflection.md)
</dt> </dl>

 

