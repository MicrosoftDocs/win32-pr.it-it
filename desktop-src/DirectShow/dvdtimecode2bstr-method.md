---
description: Il metodo DVDTimeCode2bstr recupera una stringa che indica l'ora corrente sul disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Metodo DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90bda68bafa462af5d425c62368b51f8b4b08ce2dfc310276e8f26b7c4601fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148604"
---
# <a name="dvdtimecode2bstr-method"></a>Metodo DVDTimeCode2bstr

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `DVDTimeCode2bstr` metodo recupera una stringa che indica l'ora corrente sul disco.

``` syntax
[ sTimeCode = ] MSWebDVD.DVDTimeCode2bstr(nTimeCode)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="sTimeCode"></span><span id="stimecode"></span><span id="STIMECODE"></span>*sTimeCode*
</dt> <dd>

Specifica l'ora corrente sul disco relativa all'inizio del titolo come numero ottenuto tramite l'evento [**\_ EC DVD CURRENT \_ \_ HMSF \_ TIME.**](ec-dvd-current-hmsf-time.md)

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa di 11 caratteri nel formato "hh:mm:ss:ff" che rappresenta le ore, i minuti, i secondi e i fotogrammi che definiscono l'ora corrente.

## <a name="remarks"></a>Commenti

Questo metodo è di sola lettura.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione delle notifiche degli eventi DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



