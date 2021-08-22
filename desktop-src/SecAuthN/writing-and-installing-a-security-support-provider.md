---
description: La progettazione di SSPI consente di scrivere e aggiungere altri SSP al sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Scrittura e installazione di un security support provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11ac7125c386314ec7772a5e6079f423af0aaf5c9f7dd820a24c042d99834d74
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118914750"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Scrittura e installazione di un security support provider

La progettazione di SSPI consente di scrivere e aggiungere altri SSP al sistema. Un [*provider di servizi*](../secgloss/s-gly.md) di configurazione specifico per un modello di sicurezza può essere sviluppato con relativa facilità o complessità, a seconda del livello di integrazione con il sistema operativo. Un provider di servizi di configurazione client che consente le connessioni a un nuovo tipo di server potrebbe essere sviluppato molto rapidamente, mentre un provider di servizi condivisi completo che fornisce la rappresentazione locale richiederebbe maggiore impegno.

Gli SSP vengono installati aggiornando un **valore \_ REG SZ** nel Registro di sistema, che si trova come segue:

**HKEY \_ Local \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    <dl> <dt>

            Data type
</dt> <dd>            REG \_ SZ</dd> </dl>

Una singola DLL può contenere più SSP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
