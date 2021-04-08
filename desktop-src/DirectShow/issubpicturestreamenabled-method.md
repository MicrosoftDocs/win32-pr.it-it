---
description: Il metodo IsSubpictureStreamEnabled recupera un valore che indica se il flusso di sottoimmagine specificato è abilitato nel titolo corrente.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Metodo IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 818b4ff18dac87ea3346a1a503764b2e5e9cd02a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876869"
---
# <a name="issubpicturestreamenabled-method"></a>Metodo IsSubpictureStreamEnabled

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il `IsSubpictureStreamEnabled` metodo recupera un valore che indica se il flusso di sottoimmagine specificato è abilitato nel titolo corrente.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

Specifica il flusso di sottoimmagine come intero.



| Valore   | Descrizione              |
|---------|--------------------------|
| da 0 a 31 | flusso di sottoimmagine        |
| 63      | flusso a bitrate ridotto disattivato |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se il flusso audio specificato è disponibile nel titolo corrente. True indica che è disponibile.

## <a name="remarks"></a>Commenti

Sebbene un disco possa contenere fino a 32 di flussi di immagini, ogni flusso non è necessariamente disponibile per ogni titolo. Verificare sempre che un flusso sia disponibile per un titolo prima di impostare la proprietà [**CurrentSubpictureStream**](currentsubpicturestream-property.md) .

 

 



