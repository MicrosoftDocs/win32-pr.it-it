---
title: Metodo Unload
description: Metodo Unload
ms.assetid: 2ffaeea6-ff24-48b2-bc99-eba429434a30
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f74f274f758e34416cc73d82963fa21fbd93b14e7b6492c693f24b763081b49f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118474499"
---
# <a name="unload-method"></a>Metodo Unload

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Descrizione**
</dt> <dd>

Scarica i dati di tipo carattere per il carattere specificato.

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintassi**
</dt> <dd>

*agent***. Characters.Unload "**_CharacterID_*_"_*

</dd> </dl>

## <a name="remarks"></a>Commenti

Usare questo metodo quando non è più necessario un carattere per liberare la memoria usata per archiviare le informazioni sul carattere. Se si accede di nuovo al carattere, usare il [**metodo Load.**](load-method.md)

Questo metodo non restituisce un [**oggetto Request.**](/windows/desktop/lwef/the-request-object)

 

 