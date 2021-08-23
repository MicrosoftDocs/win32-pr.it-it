---
description: Curve ellittiche abilitate nella Windows 10 versione 1607 e successive.
title: Curve ellittiche TLS in Windows 10 versione 1607 e successive
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 237d0f7a7b4b2a7fecb99a91f21c55349e7d435b221e1b3297afd1ba614cc92c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118915846"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a>Curve ellittiche TLS in Windows 10 versione 1607 e successive

Per Windows 10, versioni 1607 e successive, le curve ellittiche seguenti sono abilitate e in questo ordine di priorità per impostazione predefinita viene utilizzato il provider Microsoft Schannel:

| Stringa a curva ellittica | Disponibile in modalità FIPS |
|-------------|--------------|
| curve25519 | No |
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
