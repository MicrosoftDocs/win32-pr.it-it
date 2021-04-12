---
description: Il provider di base crea chiavi simmetriche a 40 bit create con undici byte di Salt di valore zero, undici byte di Salt diverso da zero \_ se \_ è specificato Crypt create Salt o nessun valore salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Funzionalità valore Salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344346"
---
# <a name="salt-value-functionality"></a>Funzionalità valore Salt

Il provider di base crea [*chiavi simmetriche*](../secgloss/s-gly.md) a 40 bit create con undici byte di [*Salt*](../secgloss/s-gly.md)di valore zero, undici byte di Salt diverso da zero \_ se \_ è specificato Crypt create Salt o nessun valore salt. Una chiave simmetrica a 40 bit con Salt con valore zero, tuttavia, non è equivalente a una chiave simmetrica a 40 bit senza Salt. Per l'interoperabilità, è necessario creare chiavi senza Salt. Questo problema deriva da una condizione predefinita che si verifica solo con chiavi di esattamente 40 bit. Tutte le altre [*lunghezze di chiave*](../secgloss/k-gly.md) non hanno allocato Salt per impostazione predefinita.

Sia i provider di base che il provider esteso possono usare il \_ flag crypt No \_ Salt per specificare che non viene allocato alcun valore salt per una chiave simmetrica a 40 bit. Le funzioni che accettano questo flag sono [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). Per impostazione predefinita, queste funzioni forniscono la compatibilità con le versioni precedenti per la chiave simmetrica a 40 bit continuando l'utilizzo del Salt di valore zero lungo a undici byte.

 

 
