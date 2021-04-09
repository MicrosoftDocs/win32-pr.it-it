---
description: CNG è un'API di crittografia che è possibile usare per creare software di sicurezza della crittografia per la gestione delle chiavi di crittografia, la crittografia e la sicurezza dei dati, nonché la crittografia e la sicurezza di rete.
ms.assetid: eaad88a1-4e1d-4246-9560-8eef60f8b70f
title: 'API di crittografia: prossima generazione'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d485f8371905961c63fbab66b29d0db544e3271
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878518"
---
# <a name="cryptography-api-next-generation"></a>API di crittografia: prossima generazione

## <a name="purpose"></a>Scopo

Cryptography API: Next Generation (CNG) è la sostituzione a lungo termine per [*CryptoAPI*](../secgloss/c-gly.md). CNG è progettato per essere estendibile a molti livelli ed è indipendente dalla crittografia nel comportamento.

## <a name="developer-audience"></a>Sviluppatori

CNG è progettato per essere usato dagli sviluppatori di applicazioni che consentiranno agli utenti di creare e scambiare documenti e altri dati in un ambiente protetto, soprattutto su supporti non protetti, ad esempio Internet. Gli sviluppatori devono avere familiarità con i linguaggi di programmazione C e C++ e con l'ambiente di programmazione basato su Windows. Sebbene non sia obbligatorio, è consigliabile comprendere la crittografia o gli argomenti relativi alla sicurezza.

Se si sviluppa un provider di algoritmi di crittografia CNG o un provider di archiviazione chiavi, è necessario scaricare [Cryptographic Provider Development Kit](https://www.microsoft.com/download/details.aspx?id=30688) da Microsoft.

## <a name="run-time-requirements"></a>Requisiti di runtime

CNG è supportato a partire da Windows Server 2008 e Windows Vista. Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                         | Descrizione                                                                                                                                    |
|-----------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni su CNG](about-cng.md)<br/>         | Descrive le funzionalità CNG, le primitive crittografiche e l'archiviazione delle chiavi, il recupero, l'importazione e l'esportazione.<br/>                                   |
| [Uso di CNG](using-cng.md)<br/>         | Viene illustrato come utilizzare le funzionalità di configurazione della crittografia di CNG e la tipica programmazione CNG.<br/>                                     |
| [Riferimento CNG](cng-reference.md)<br/> | Descrizioni dettagliate degli elementi di programmazione CNG. Queste pagine includono descrizioni di riferimento dell'API per l'uso di CNG. <br/> |



 

 

