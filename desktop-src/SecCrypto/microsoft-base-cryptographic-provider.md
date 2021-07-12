---
description: Microsoft Base Cryptographic Provider è il provider del provider del servizio di crittografia (CSP) iniziale e viene distribuito con CryptoAPI versioni 1.0 e 2.0. Si tratta di un provider per utilizzo generico che supporta le firme digitali e la crittografia dei dati.
ms.assetid: c36025c5-a407-4a05-8780-23f8107730df
title: Provider del servizio di crittografia Microsoft Base
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d53bd4b2f7faf140e57d25b54d3161b47dcaf740
ms.sourcegitcommit: 822413efb4a70dd464e5db4d9e8693ef74f8132f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 07/09/2021
ms.locfileid: "113581889"
---
# <a name="microsoft-base-cryptographic-provider"></a>Provider del servizio di crittografia Microsoft Base

Microsoft Base Cryptographic Provider è il [*provider*](../secgloss/c-gly.md) del provider del servizio di crittografia (CSP) iniziale e viene distribuito con [*CryptoAPI*](../secgloss/c-gly.md) versioni 1.0 e 2.0. Si tratta di un provider per utilizzo generico che supporta le [*firme digitali e*](../secgloss/d-gly.md) la crittografia dei dati.

L'algoritmo a chiave pubblica RSA viene usato per tutte le operazioni con chiave pubblica.

Per mantenere la compatibilità con le versioni precedenti, la nuova versione del provider mantiene la designazione della versione 1.0 del nome in Wincrypt.h. Tuttavia, la versione 2.0 di questo provider è attualmente disponibile. Per determinare la versione effettiva del provider in uso, chiamare [**CryptGetProvParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam) con l'argomento *dwParam* impostato su **PP \_ VERSION.** Se 0x0200 viene restituito in *pbData*, si ha la versione 2.0.

|                   | Valore            |
|-------------------|------------------|
| **Tipo provider** | PROV \_ RSA \_ FULL  |
| **Nome provider** | MS \_ DEF \_ PROV    |



 

 

 
