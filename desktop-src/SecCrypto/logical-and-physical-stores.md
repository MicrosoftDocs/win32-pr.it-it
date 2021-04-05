---
description: Gli archivi di sistema predefiniti, inclusi MY, CA e ROOT, vengono implementati come archivi di raccolte logiche con diversi archivi fisici predefiniti come archivi membri.
ms.assetid: 1d82b94b-4842-454a-aca4-823cd264ac52
title: Archivi logici e fisici
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 66a5441bac91e39b7f4c124daecd3a6a569c323c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752138"
---
# <a name="logical-and-physical-stores"></a>Archivi logici e fisici

Gli archivi di sistema predefiniti, inclusi MY, CA e ROOT, vengono implementati come archivi di raccolte logiche con diversi archivi fisici predefiniti come archivi membri. Gli archivi fisici dei membri di un archivio di sistema vengono aperti automaticamente al momento dell'apertura dell'archivio di sistema. Un utente può aggiungere altri archivi fisici a qualsiasi raccolta di archivi di sistema. La funzione CryptoAPI [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore) aggiunge un nuovo archivio fisico a una raccolta di archivi di sistema. [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore) Annulla l'associazione di un archivio fisico da un archivio di sistema logico. [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore) crea un nuovo archivio di sistema in un HKEY del registro di sistema, mentre [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore) rimuove un archivio di sistema dal registro di sistema.

In CryptoAPI gli archivi di sistema sono archivi logici con archivi fisici associati. Tutti i certificati in un archivio di sistema esistente rimangono disponibili e l'aggiunta fisica di nuovi certificati viene eseguita negli archivi fisici che costituiscono l'archivio di sistema logico.

Gli utenti che preferiscono continuare a usare gli archivi di sistema fisici e non convertirli in archivi logici possono aprire gli archivi di sistema con il \_ \_ \_ provider del registro di sistema CERT Store prov \_ . Questo provider continuerà a usare ogni archivio di sistema come singolo archivio fisico.

Le funzioni [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation), [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)e [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) elencano i percorsi di archivio del sistema, gli archivi di sistema disponibili e tutti gli archivi fisici che sono membri di un archivio di sistema.

È anche possibile rilocare gli archivi di sistema. Per impostazione predefinita, viene aperto un archivio di sistema relativo a una sottochiave del registro di sistema che segue un criterio predefinito. Per ulteriori informazioni, vedere [percorsi di archivio di sistema](system-store-locations.md). L'impostazione \_ del \_ flag di rilocazione dell'archivio di sistema CERT \_ \_ nel parametro *dwFlags* passato a [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) posiziona un archivio di sistema nel registro di sistema in una sottochiave del registro di sistema specificata dall'utente anziché in quella predefinita.

 

 



