---
title: Barra della lingua (applicazioni TSF)
description: Un'applicazione non può aggiungere elementi alla barra della lingua; solo un servizio di testo può aggiungere elementi alla barra della lingua.
ms.assetid: facb0da1-3f80-4745-b021-c026e7e5356c
keywords:
- Framework servizi di testo (TSF), barra della lingua
- TSF (Framework dei servizi di testo), barra della lingua
- Applicazioni abilitate per TSF, barra della lingua
- barra della lingua
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef227b29c8b481bfaefc4a218305ba8974fe54e2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "103873249"
---
# <a name="language-bar-tsf-applications"></a>Barra della lingua (applicazioni TSF)

Un'applicazione non può aggiungere elementi alla barra della lingua; solo un servizio di testo può aggiungere elementi alla barra della lingua. Un'applicazione può influire sulla modalità di visualizzazione di determinati elementi sulla barra della lingua.

Il raggruppamento di [ \_ \_ \_ DICTATIONSTAT](predefined-compartments.md) per la voce del raggruppamento GUID viene usato per indicare il tipo di input vocale che l'applicazione può accettare: input di testo diretto (dettatura) e/o comandi vocali. Per impostazione predefinita, la dettatura è abilitata e il comando Voice è disabilitato. Se l'applicazione è in grado di accettare comandi vocali, deve impostare il valore [ \_ \_ abilitato per il comando tf](speech-recognition-constants.md) nel raggruppamento DICTATIONSTAT del dialogo del raggruppamento dei GUID \_ \_ \_ . Se l'applicazione è in grado di accettare la dettatura, deve impostare il \_ \_ valore abilitato per la dettatura di TF nel raggruppamento DICTATIONSTAT della voce del raggruppamento GUID \_ \_ \_ . La \_ dettatura del TF \_ o il \_ comando tf \_ sul valore di questo raggruppamento determina l'input vocale della modalità (dettatura o comando) attualmente in.

Se l'applicazione supporta l'archiviazione permanente dei dati delle proprietà, è necessario impostare il raggruppamento [GUID \_ \_ PERSISTMENUENABLED](predefined-compartments.md) raggruppamento su un valore diverso da zero. Questo fa sì che il servizio di testo vocale consenta la voce di menu **Salva dati vocali** .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Come configurare il Framework dei servizi di testo](how-to-set-up-tsf.md)
</dt> <dt>

[Barra della lingua (servizi di testo)](language-bar.md)
</dt> </dl>

 

 




