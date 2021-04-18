---
description: Il metodo DVDTimeCode2bstr recupera una stringa che indica l'ora corrente del disco.
ms.assetid: 0a477274-ac56-4f46-8461-53411362b33e
title: Metodo DVDTimeCode2bstr
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 042c6889fd2d5ee76aa42fc4e92f1c2754a5c95d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304010"
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

Specifica l'ora corrente del disco rispetto all'inizio del titolo come numero ottenuto tramite l'evento di [**\_ \_ \_ \_ ora HMSF corrente del DVD EC**](ec-dvd-current-hmsf-time.md) .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce una stringa di 11 caratteri nel formato "HH: mm: SS: FF" che rappresenta le ore, i minuti, i secondi e i frame che definiscono l'ora corrente.

## <a name="remarks"></a>Commenti

Questo metodo è di sola lettura.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Gestione delle notifiche degli eventi DVD](handling-dvd-event-notifications.md)
</dt> </dl>

 

 



