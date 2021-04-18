---
description: Gestione dello schema di risparmio energia
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Gestione dello schema di risparmio energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 867d7509e9a04e948818ff7a3a13638a5c9933b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312042"
---
# <a name="power-scheme-management"></a>Gestione dello schema di risparmio energia

Ogni combinazione di energia viene identificata in modo univoco da un **GUID**. Per enumerare tutte le combinazioni per il risparmio di energia disponibili, usare la funzione [**PowerEnumerate**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) . **PowerEnumerate** può essere usato anche per recuperare tutte le impostazioni di risparmio energia per uno schema specificato.

Lo schema di risparmio energia attualmente in uso nel sistema è denominato schema di risparmio energia attivo o piano. Per recuperare il **GUID** del piano attivo, chiamare la funzione [**PowerGetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) . Per modificare la combinazione per il risparmio di energia attiva, chiamare la funzione [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) .

Per creare uno schema di risparmio energia, è necessario innanzitutto duplicare uno schema esistente usando la funzione [**PowerDuplicateScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) , specificando il **GUID** dello schema su cui si desidera basare il nuovo schema. È necessario copiare uno degli schemi predefiniti e modificare le impostazioni di risparmio energia in base alle esigenze. Si noti che la creazione di una combinazione per il risparmio di energia non aggiorna automaticamente il risparmio di energia attivo. È sempre necessario chiamare [**PowerSetActiveScheme**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) per aggiornare la combinazione per il risparmio di energia attiva. Le combinazioni per il risparmio di energia esistenti possono essere modificate e quindi applicate nello stesso modo.

Per rimuovere una combinazione per il risparmio di energia, chiamare la funzione [**PowerDeleteScheme**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme) .

> [!Note]  
> Per recuperare informazioni aggiuntive sullo stato di alimentazione del sistema, chiamare la funzione [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation) .

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazioni per il risparmio di energia](power-schemes.md)
</dt> </dl>

 

 



