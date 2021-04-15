---
title: Tag LST
description: Tag LST
ms.assetid: 82246675-9aa1-4603-a8f7-a5fd7b3f6be2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecf13da7bf0267941939ec22c12706ed8c75c27e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104515748"
---
# <a name="lst-tag"></a>Tag LST

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Ripete l'ultima istruzione pronunciata per il carattere.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

\\**LST**\\

</dd> </dl>

### <a name="remarks"></a>Commenti

Questo tag consente a un carattere di ripetere l'ultima istruzione pronunciata. Questo tag deve essere visualizzato da solo nel metodo [**Speak**](speak-method.md) ; non è possibile includere altri parametri o testo. Quando il testo parlato viene ripetuto, tutti gli altri tag inclusi nel testo originale vengono ripetuti, ad eccezione dei segnalibri. Qualsiasi. WAV e. Vengono ripetuti anche i file LWV inclusi nel testo.

 

 




