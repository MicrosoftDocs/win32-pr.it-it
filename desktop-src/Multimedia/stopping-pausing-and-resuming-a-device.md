---
title: Arresto, sospensione e ripresa di un dispositivo
description: Arresto, sospensione e ripresa di un dispositivo
ms.assetid: df9ca4ab-4711-44dd-a058-909f291a1652
keywords:
- MCI_STOP comando
- MCI_PAUSE comando
- MCI_RESUME comando
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5485365a6c846556a1037f55a0b211755ce0f93162bc6720c7241353fc8625b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037101"
---
# <a name="stopping-pausing-and-resuming-a-device"></a>Arresto, sospensione e ripresa di un dispositivo

Il [**comando stop**](stop.md) ([**MCI \_ STOP**](mci-stop.md)) sospende la riproduzione o la registrazione di un dispositivo. Molti dispositivi supportano anche [**il comando pause**](pause.md) ([**MCI \_ PAUSE).**](mci-pause.md) La differenza tra **arresto** **e sospensione** dipende dal dispositivo. In **genere la sospensione** sospende l'operazione, ma lascia il dispositivo pronto per riprendere immediatamente la riproduzione o la registrazione.

L'uso del comando play [**(**](play.md) [**MCI \_ PLAY**](mci-play.md)) o [**record**](record.md) ([**MCI \_ RECORD**](mci-record.md)) per riavviare un dispositivo reimposta le posizioni specificate con i flag "to" (MCI TO) e \_ "from" (MCI FROM) prima della sospensione o dell'arresto del \_ dispositivo. Senza il flag "from", questi comandi reimpostano la posizione iniziale sulla posizione corrente. Senza il flag "to", reimpostano la posizione finale alla fine del supporto. Per continuare la riproduzione o la registrazione senza  reimpostare  una posizione di arresto specificata in precedenza, usare il flag "to" del comando di riproduzione o registrazione per specificare una posizione finale.

Alcuni dispositivi supportano [**il comando resume**](resume.md) [**(MCI \_ RESUME)**](mci-resume.md)per riavviare un dispositivo sospeso. Questo comando non modifica i percorsi "to" e "from" specificati con il comando **play** o **record** che precedeva [**il comando pause.**](pause.md)

 

 




