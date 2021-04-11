---
description: Curve ellittiche abilitate in Windows 10 versione 1607 e successive.
title: Curve di TLS ellittiche in Windows 10 versione 1607 e successive
ms.topic: article
ms.keywords: ecc curves, elliptic curves, tls elliptic curves, ECC curves, schannel, ECC, EC, Elliptic Curve Cryptography
ms.date: 06/10/2020
ms.openlocfilehash: 813a7c117f5f1e3fc1c6484fc57d1c9f14cf9567
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232953"
---
# <a name="tls-elliptic-curves-in-windows-10-version-1607-and-later"></a>Curve di TLS ellittiche in Windows 10 versione 1607 e successive

Per Windows 10, versioni 1607 e successive, le seguenti curve ellittiche sono abilitate e in questo ordine di priorità per impostazione predefinita tramite il provider Microsoft Schannel:

| Stringa a curva ellittica | Disponibile in modalità FIPS |
|-------------|--------------|
| curve25519 | No |
| NistP256 | Sì |
| NistP384 | Sì |


Le seguenti curve ellittiche sono supportate dal provider Microsoft Schannel, ma non sono abilitate per impostazione predefinita:

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



## <a name="enabling-elliptic-curves"></a>Abilitazione di curve ellittiche

Per aggiungere curve ellittiche, distribuire un criterio di gruppo o usare i cmdlet di TLS:
- Per usare criteri di gruppo, [configurare l'ordine di curva ecc](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order) in configurazione Computer > modelli amministrativi > rete > impostazioni di configurazione SSL con l'elenco di priorità per tutte le curve ellittiche che si vuole abilitare.

- Per usare PowerShell, vedere [cmdlet TLS](/powershell/module/tls) per un elenco completo della sintassi e delle descrizioni dei cmdlet TLS.


> [!NOTE]
> Prima di Windows 10, le stringhe del pacchetto di crittografia venivano aggiunte con la curva ellittica per determinare la priorità della curva. Windows 10 supporta un'impostazione dell'ordine di priorità a curva ellittica, quindi il suffisso della curva ellittica non è obbligatorio e viene sostituito dal nuovo ordine di priorità della curva ellittica, se specificato, per consentire alle organizzazioni di utilizzare criteri di gruppo per configurare versioni diverse di Windows con gli stessi pacchetti di crittografia.


## <a name="see-also"></a>Vedere anche

[Configurazione dell'ordine delle curve TLS ECC](/windows-server/security/tls/manage-tls#configuring-tls-ecc-curve-order)

[Gestione dell'ordine di TLS](/windows-server/security/tls/manage-tls#managing-tls-ecc-order)

[Gestione delle curve ECC di Windows con Criteri di gruppo](/windows-server/security/tls/manage-tls#managing-windows-ecc-curves-using-group-policy)

[Cmdlet TLS](/powershell/module/tls)
