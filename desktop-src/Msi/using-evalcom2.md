---
description: Evalcom2.dll può essere usato per implementare le operazioni di convalida per i pacchetti di installazione e unire i moduli usando gli analizzatori di coerenza interni-CIEM.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Uso di Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751695"
---
# <a name="using-evalcom2"></a>Uso di Evalcom2

Evalcom2.dll può essere usato per implementare le operazioni di convalida per i pacchetti di installazione e unire i moduli usando gli [analizzatori di coerenza interni-CIEM](internal-consistency-evaluators-ices.md). L'oggetto Main implementa le interfacce per i programmi C/C++.

L'oggetto Main implementa anche le [interfacce Evalcom2](evalcom2-interfaces.md) per i programmi C/C++. Il CLSID necessario per ottenere l'interfaccia da [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) è {6E5E1910-8053-4660-B795-6B612E29BC58}. REFIID è {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.

Per implementare le operazioni di convalida, è possibile utilizzare la procedura riportata di seguito.

**Per implementare le operazioni di convalida**

1.  Inizializzare COM sul thread chiamante usando [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).
2.  Ottenere il puntatore all'interfaccia [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) utilizzando [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).
3.  Aprire il pacchetto di installazione o il modulo merge usando il metodo [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) .
4.  Aprire il file di valutazione usando il metodo [**OpenCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) .
5.  Impostare la funzione di callback di visualizzazione utilizzando il metodo di [**visualizzazione**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) .
6.  Impostare la funzione di callback dello stato usando il metodo [**sestatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) .
7.  Eseguire la convalida usando il metodo [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) .
8.  Chiudere il file con estensione cub usando il metodo [**CloseCUB**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) .
9.  Chiudere il database utilizzando il metodo [**ChiudiDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) .
10. Rilasciare l'interfaccia [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) .
11. Annullare l'inizializzazione di COM con [**CoUninitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce Evalcom2](evalcom2-interfaces.md)
</dt> <dt>

[Automazione della convalida](validation-automation.md)
</dt> <dt>

[Funzioni di callback di convalida](validation-callback-functions.md)
</dt> </dl>

 

 
