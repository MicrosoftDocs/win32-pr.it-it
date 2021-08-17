---
description: Gestione di combinazioni per il risparmio di energia
ms.assetid: b79e7b64-be56-4165-af59-a8251284d029
title: Gestione di combinazioni per il risparmio di energia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ab4717fd8efc91a520e178baac6ad9138028f306386ed2ee1141b76a423b16e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143404"
---
# <a name="power-scheme-management"></a>Gestione di combinazioni per il risparmio di energia

Ogni combinazione per il risparmio di energia è identificata in modo univoco da **un GUID**. Per enumerare tutte le combinazioni per il risparmio di energia disponibili, usare la [**funzione PowerEnumerate.**](/windows/desktop/api/PowrProf/nf-powrprof-powerenumerate) **PowerEnumerate** può essere usato anche per recuperare tutte le impostazioni di risparmio energia per uno schema specificato.

La combinazione per il risparmio di energia attualmente in uso nel sistema è detta combinazione o combinazione per il risparmio di energia attiva. Per recuperare il **GUID** del piano attivo, chiamare la [**funzione PowerGetActiveScheme.**](/windows/desktop/api/Powersetting/nf-powersetting-powergetactivescheme) Per modificare la combinazione per il risparmio di energia attiva, chiamare la [**funzione PowerSetActiveScheme.**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme)

Per creare una combinazione per il risparmio di energia, è innanzitutto necessario duplicare uno schema esistente usando la funzione [**PowerDuplicateScheme,**](/windows/desktop/api/PowrProf/nf-powrprof-powerduplicatescheme) specificando il **GUID** dello schema su cui si vuole basare il nuovo schema. È necessario copiare uno degli schemi predefiniti e modificare le impostazioni di risparmio energia in base alle esigenze. Si noti che la creazione di una combinazione per il risparmio di energia non aggiorna automaticamente la combinazione per il risparmio di energia attiva. È sempre necessario chiamare [**PowerSetActiveScheme per**](/windows/desktop/api/Powersetting/nf-powersetting-powersetactivescheme) aggiornare la combinazione per il risparmio di energia attiva. Le combinazioni per il risparmio di energia esistenti possono essere modificate e quindi applicate nello stesso modo.

Per rimuovere una combinazione per il risparmio di energia, chiamare la [**funzione PowerDeleteScheme.**](/windows/desktop/api/PowrProf/nf-powrprof-powerdeletescheme)

> [!Note]  
> Per recuperare informazioni aggiuntive sullo stato di alimentazione del sistema, chiamare la [**funzione CallNtPowerInformation.**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Combinazioni per il risparmio di energia](power-schemes.md)
</dt> </dl>

 

 



