---
description: Il pacchetto di autenticazione Kerberos viene utilizzato per l'accesso a una rete. gli accessi locali vengono gestiti da MSV1 \_ 0.
ms.assetid: 43970c99-53f1-43c1-9d9f-65573572f731
title: SSP/AP Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d14565c8c6526d9cab34d7b9ddec9a0a04ff8de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050139"
---
# <a name="kerberos-sspap"></a>SSP/AP Kerberos

Il pacchetto di autenticazione [*Kerberos*](../secgloss/k-gly.md) viene utilizzato per l'accesso a una rete. gli accessi locali vengono gestiti da MSV1 \_ 0.

Quando un utente esegue l'accesso utilizzando un account di rete, per impostazione predefinita Kerberos tenta di connettersi al [*centro distribuzione chiavi*](../secgloss/k-gly.md) Kerberos (KDC) sul controller di dominio e di ottenere un ticket di concessione ticket (TGT) utilizzando i dati di accesso forniti dall'utente.

Se un KDC Kerberos non è disponibile, Windows usa MSV1 \_ 0 e l'autenticazione pass-through come descritto [nel \_ pacchetto di autenticazione MSV1 0](msv1-0-authentication-package.md).

Il pacchetto di autenticazione Kerberos supporta la versione 5, Revisione 6 del protocollo Kerberos. Questo protocollo si basa su Internet [RFC 4120](https://www.ietf.org/rfc/rfc4120.txt). Per ulteriori informazioni, vedere il sito Web IETF:

[https://www.ietf.org](https://www.ietf.org/)

Per ulteriori informazioni su Kerberos, vedere [Microsoft Kerberos](microsoft-kerberos.md).

## <a name="kerberos-credential-formats"></a>Formati di credenziali Kerberos

Le [*credenziali*](../secgloss/c-gly.md) utente assegnate dal pacchetto di autenticazione Kerberos dopo un tentativo di accesso riuscito sono un ticket e una chiave di crittografia temporanea, spesso detta [*chiave di sessione*](../secgloss/s-gly.md). Il ticket contiene una copia crittografata delle credenziali del client e della chiave della sessione.

 

 
