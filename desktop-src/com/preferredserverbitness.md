---
title: PreferredServerBitness
description: Imposta l'architettura preferita, a 32 bit o a 64 bit, per questo server COM.
ms.assetid: ef770039-1624-4256-aa09-1443695c1a1f
keywords:
- Valore PreferredServerBitness del registro di sistema COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 107a8c5b1504c5a59ca2ab178cd46236335d44ca
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104339358"
---
# <a name="preferredserverbitness"></a>PreferredServerBitness

Imposta l'architettura preferita, a 32 bit o a 64 bit, per questo server COM.

## <a name="registry-entry"></a>Voce del Registro di sistema

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      PreferredServerBitness = value
```

## <a name="remarks"></a>Commenti

Si tratta di un valore **reg \_ DWORD** disponibile solo nelle versioni di Windows a 64 bit.



| Valore | Descrizione                                                                                                                                                                                                |
|-------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1     | Abbinare l'architettura del server all'architettura client. Se, ad esempio, il client è a 32 bit, utilizzare una versione a 32 bit del server, se disponibile. In caso contrario, la richiesta di attivazione del client avrà esito negativo. |
| 2     | Usare una versione a 32 bit del server. Se non ne esiste una, la richiesta di attivazione del client avrà esito negativo.                                                                                                      |
| 3     | Usare una versione a 64 bit del server. Se non ne esiste una, la richiesta di attivazione del client avrà esito negativo.                                                                                                      |



 

Se questo valore non è presente, eseguire le operazioni seguenti:

-   Se nel computer che ospita il server è in esecuzione Windows XP o Windows Server 2003 senza SP1 o versione successiva, è preferibile a una versione a 64 bit del server, se disponibile. in caso contrario, attiverà una versione a 32 bit del server.
-   Se nel computer che ospita il server è in esecuzione Windows Server 2003 con SP1 o versione successiva, COM tenterà di abbinare l'architettura del server all'architettura client. In altre parole, per un client a 32 bit, COM attiverà un server a 32 bit, se disponibile. in caso contrario, attiverà una versione a 64 bit del server. Per un client a 64 bit, COM attiverà un server a 64 bit se disponibile; in caso contrario, attiverà un server a 32 bit.

Il client può anche specificare la propria preferenza di architettura tramite il \_ Server CLSCTX activate \_ 32 \_ bit \_ e CLSCTX \_ Activate \_ 64 \_ bit \_ Server Flags, che sostituiranno le preferenze del server. Per ulteriori informazioni e un grafico delle possibili interazioni tra le preferenze per l'architettura client e server, vedere [**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CLSCTX**](/windows/win32/api/wtypesbase/ne-wtypesbase-clsctx)
</dt> </dl>

 

 