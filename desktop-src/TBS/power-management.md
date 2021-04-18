---
title: Risparmio energia (servizi di base TPM)
description: TBS riceve gli eventi di risparmio energia.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: 8ea1a82717bd3dbb3457be0697329aa37fb13f08
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/11/2019
ms.locfileid: "106299327"
---
# <a name="power-management-tpm-base-services"></a>Risparmio energia (servizi di base TPM)

TBS riceve gli eventi di risparmio energia. Quando viene ricevuta un'indicazione che il TPM o altre parti della piattaforma stanno per entrare in uno stato di alimentazione in cui l'esecuzione verrà interrotta o lo stato del TPM andrà perduto, TBS controlla per determinare se è probabile che il comando attualmente in esecuzione venga terminato prima che il sistema venga disattivato. In generale, TBS consente il completamento dei comandi di durata breve e media, ma annulla i comandi a lunga durata. Dopo che il comando ha restituito, TBS interrompe l'invio di nuovi comandi al TPM e si prepara per l'ibernazione. Quando viene ripristinata l'alimentazione, TBS restituisce il risultato del comando al chiamante, quindi procede con l'elaborazione dei comandi TBS in sospeso. Il codice di risparmio energia di TBS viene eseguito in modo asincrono, quindi può gestire le richieste di risparmio energia anche se il TPM sta elaborando un comando lungo.

Quando un computer immette gli Stati di sospensione, inclusi S3 (sospensione) e S4 (ibernazione), il TPM è spento. Quindi, tutti gli Stati del TPM non permanenti vengono persi. Prima di immettere questi Stati, è previsto che il software dell'applicazione si prepari alla perdita di stati TPM volatili. Quando il sistema torna da uno stato di sospensione, TBS si sincronizza con il TPM in modo che lo stato di TBS sia coerente con lo stato TPM. Potrebbe essere necessario riemettere i comandi interrotti dal software dell'applicazione.

 

 




