---
description: Crea una richiesta PKCS \# 10 personalizzata e tenta di registrarla in un'autorità di certificazione (CA) dell'organizzazione (Enterprise).
ms.assetid: ACBD3CE1-6A2A-47EE-9482-7398ABE15F5C
title: enrollCustomPKCS10_2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d20615826bb72b6282144b72a394cde41e35910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308121"
---
# <a name="enrollcustompkcs10_2"></a>enrollCustomPKCS10 \_ 2

L' \_ esempio enrollCustomPKCS10 2 crea una richiesta PKCS \# 10 personalizzata e tenta di registrarla in un' [*autorità di certificazione*](/windows/desktop/SecGloss/c-gly) (CA) dell'organizzazione (Enterprise).

## <a name="location"></a>Location

Quando si installa il Software Development Kit (SDK) di Microsoft Windows, l'esempio viene installato per impostazione predefinita nella cartella *% ProgramFiles%* \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Security \\ X509 certificate \\ VC \\ enrollCustomPKCS10 \_ 2.

## <a name="discussion"></a>Discussione

Esempio enrollCustomPKCS10 \_ 2:

1.  Elabora gli argomenti della riga di comando. La riga di comando deve contenere il nome di un modello e il nome di un provider di crittografia.
2.  Crea un oggetto [**metodo IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) e lo inizializza usando il nome del modello specificato nella riga di comando.
3.  Recupera la [*richiesta di certificato*](/windows/desktop/SecGloss/c-gly) dall'oggetto di registrazione.
4.  Recupera la richiesta PKCS \# 10 più interna dall'oggetto richiesta di certificato ottenuto nel passaggio 3.
5.  Recupera una [*chiave privata*](/windows/desktop/SecGloss/p-gly) dalla richiesta PKCS \# 10.
6.  Crea una raccolta [**ICspInformations**](/windows/desktop/api/CertEnroll/nn-certenroll-icspinformations) e aggiunge i provider di crittografia disponibili alla raccolta e quindi recupera un oggetto [**ICspStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-icspstatus) per il provider specificato nella riga di comando.
7.  Imposta l'oggetto stato sulla chiave privata.
8.  Tenta di registrare la [*richiesta di certificato*](/windows/desktop/SecGloss/c-gly).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[\#Richiesta PKCS 10](pkcs--10-request.md)
</dt> <dt>

[Uso degli esempi inclusi](using-the-included-samples.md)
</dt> </dl>

 

 
