---
description: La progettazione di SSPI consente la scrittura e l'aggiunta di SSP aggiuntivi al sistema.
ms.assetid: 0d462340-e485-4746-b627-d823752462d9
title: Scrittura e installazione di un Security Support Provider
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e19f827ddf2b0352acc889df3ed1d5b3dfff52c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313726"
---
# <a name="writing-and-installing-a-security-support-provider"></a>Scrittura e installazione di un Security Support Provider

La progettazione di SSPI consente la scrittura e l'aggiunta di SSP aggiuntivi al sistema. Un [*SSP*](../secgloss/s-gly.md) specifico di un modello di sicurezza può essere sviluppato con la relativa semplicità o complessità elevata, a seconda del livello di integrazione con il sistema operativo. Un SSP client che consente di stabilire connessioni a un nuovo tipo di server può essere sviluppato molto rapidamente, mentre un SSP completo che fornisce la rappresentazione locale richiederebbe maggiore sforzo.

I provider di servizi condivisi vengono installati aggiornando un valore **reg \_ SZ** nel registro di sistema, disponibile nel modo seguente:

**HKEY \_ \_Computer locale** \\ **System** \\ **CurrentControlSet** \\ **Control** \\ **SecurityProviders**  =  *Provider1.dll, Provider2.dll,*...    <dl> <dt>

            Data type
</dt> <dd>            REG \_ SZ</dd> </dl>

Una singola DLL può contenere più SSP.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Restrizioni relative alla registrazione e all'installazione di un pacchetto di sicurezza](restrictions-around-registering-and-installing-a-security-package.md)
</dt> </dl>

 

 
