---
description: Le curve ellittiche abilitate nelle Windows 10 1507 e 1511.
title: Curve ellittiche TLS nelle Windows 10 1507 e 1511
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 91dfc7dac8f45b9c4f2231f6db93e776c75544373199170146f55362f02f2be3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915866"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1507-and-1511"></a>Curve ellittiche TLS nelle Windows 10 1507 e 1511

Per Windows 10, versioni 1507 e 1511, le curve ellittiche seguenti sono abilitate e in questo ordine di priorità per impostazione predefinita tramite il provider Microsoft Schannel:

| Stringa a curva ellittica | Disponibile in modalità FIPS |
|-------------|--------------|
| NistP256 | Sì |
| NistP384 | Sì |


Le curve ellittiche seguenti sono supportate dal provider Microsoft Schannel, ma non sono abilitate per impostazione predefinita:

| Stringa a curva ellittica | Disponibile in modalità FIPS |
|-------------|--------------|
| brainpoolP256r1 | No |
| brainpoolP384r1 | No |
| brainpoolP512r1 | No |
| nistP192 | No |
| nistP224 | No |
| nistP521 | Sì |
| secP160k1 | No |
| secP160r1 | No |
| secP160r2 | No |
| secP192k1 | No |
| secP192r1 | No |
| secP224k1 | No |
| secP224r1 | No |
| secP256k1 | No |
| secP256r1 | No |
| secP384r1 | No |
| secP521r1 | No |

## <a name="enabling-elliptic-curves"></a>Abilitazione delle curve ellittiche

Per aggiungere curve ellittiche, distribuire criteri di gruppo o usare i cmdlet TLS:
- Per usare Criteri di gruppo, configurare [ECC Curve Order](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) in Configurazione computer > Modelli amministrativi > Rete > Ssl Configuration Impostazioni con l'elenco di priorità per tutte le curve ellittiche che si desidera sia abilitato.

- Per usare PowerShell, vedere [Cmdlet TLS per](/powershell/module/tls) un elenco completo della sintassi e delle descrizioni dei cmdlet TLS.


> [!NOTE]
> Prima di Windows 10, le stringhe del gruppo di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva. Windows 10 supporta un'impostazione dell'ordine di priorità a curva ellittica in modo che il suffisso a curva ellittica non sia obbligatorio e venga sostituito dal nuovo ordine di priorità a curva ellittica, se specificato, per consentire alle organizzazioni di usare Criteri di gruppo per configurare versioni diverse di Windows con gli stessi pacchetti di crittografia.


## <a name="see-also"></a>Vedere anche

[Configurazione dell'ordine delle curve ECC TLS](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Gestione dell'ordine ECC TLS](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Gestione Windows curve ECC tramite Criteri di gruppo](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Cmdlet TLS](/powershell/module/tls)
