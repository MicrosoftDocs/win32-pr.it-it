---
title: Creazione di dischi con più sessioni
description: IMAPI è in grado di creare dischi dati multi-sessione. Quando si crea un disco con più sessioni, è necessario tenere presenti alcune considerazioni.
ms.assetid: 02405a32-53d5-4618-bfa0-c9a9f5e3c51b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7477b108a6b7b07d6d82230362899da26e7264e62a460c197338e223f0e95078
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977121"
---
# <a name="creating-discs-with-multiple-sessions"></a>Creazione di dischi con più sessioni

IMAPI è in grado di creare dischi dati multi-sessione. Quando si crea un disco con più sessioni, è necessario tenere presenti alcune considerazioni.

Il [**metodo IDiscMaster::SetActiveDiscRecorder**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-setactivediscrecorder) determina se è presente un disco multi-sessione IMAPI nell'unità attiva al momento dell'impostazione. In tal caso, IMAPI passa automaticamente alla modalità multi-sessione. Se [**si usa ClearFormatContent**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-clearformatcontent) dopo che è stata stabilita la modalità multi-sessione, IMAPI torna alla modalità a sessione singola. Ciò significa che è necessario un disco vuoto per una [**masterizzazione RecordDisc.**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc) Se il disco è in modalità multi-sessione, lo stesso disco deve essere nel registratore attivo oppure verrà restituito un codice di errore IMAPI \_ E \_ WRONGDISC.

Se si seleziona un registratore in formato Joliet, IMAPI legge le informazioni dal disco attualmente installato. Se il disco è un disco IMAPI Joliet precedente con spazio per un'altra sessione, IMAPI imposta automaticamente se stesso sulla modalità multi-sessione. Questo disco deve essere presente nel registratore attivo quando si chiama [**RecordDisc**](/windows/desktop/api/Imapi/nf-imapi-idiscmaster-recorddisc).

La chiusura della prima sessione su un disco richiede 21 MB. Ogni sessione aggiuntiva richiede 11 MB per la chiusura.

 

 




