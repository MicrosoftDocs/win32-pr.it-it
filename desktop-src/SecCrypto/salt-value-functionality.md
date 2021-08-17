---
description: Il provider di base crea chiavi simmetriche a 40 bit create con 11 byte di salt con valore zero, 11 byte di salt diverso da zero se viene specificato CRYPT CREATE SALT o nessun valore \_ \_ salt.
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Funzionalità del valore salt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f911815152861921f1ffe12090c88ad4795ba042346aee875138acf591d14671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900371"
---
# <a name="salt-value-functionality"></a>Funzionalità del valore salt

Il provider di base crea chiavi simmetriche a 40 [*bit*](../secgloss/s-gly.md) create con 11 byte di [*salt*](../secgloss/s-gly.md)con valore zero, 11 byte di salt diverso da zero se viene specificato CRYPT CREATE SALT o nessun valore \_ \_ salt. Una chiave simmetrica a 40 bit con salt di valore zero, tuttavia, non equivale a una chiave simmetrica a 40 bit senza salt. Per l'interoperabilità, le chiavi devono essere create senza salt. Questo problema deriva da una condizione predefinita che si verifica solo con chiavi di esattamente 40 bit. Per tutte [*le altre lunghezze di chiave*](../secgloss/k-gly.md) non è allocato il salt per impostazione predefinita.

Sia i provider di base che il provider esteso possono usare il flag CRYPT NO SALT per specificare che non viene allocato alcun valore salt per una chiave \_ \_ simmetrica a 40 bit. Le funzioni che accettano questo flag sono [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey), [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)e [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey). Per impostazione predefinita, queste funzioni forniscono la compatibilità con le versioni precedenti per la combinazione di maiuscole e minuscole simmetriche a 40 bit continuando l'uso del salt di valore zero a 11 byte.

 

 
