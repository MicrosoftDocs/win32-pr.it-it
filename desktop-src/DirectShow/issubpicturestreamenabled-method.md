---
description: Il metodo IsSubpictureStreamEnabled recupera un valore che indica se il flusso di immagini secondarie specificato è abilitato nel titolo corrente.
ms.assetid: c6436f77-ca94-464f-9336-f485f5d5d199
title: Metodo IsSubpictureStreamEnabled
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc982120b6a7a57d59d5213fc57b5ba3851d7d9d2f4c3e553fba97d3307d8bec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117817048"
---
# <a name="issubpicturestreamenabled-method"></a>Metodo IsSubpictureStreamEnabled

> [!Note]  
> Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003. È possibile che in versioni successive sia stata modificata o non sia più disponibile.

 

Il metodo recupera un valore che indica se il flusso di immagini secondarie specificato `IsSubpictureStreamEnabled` è abilitato nel titolo corrente.

``` syntax
[ bEnabled = ] MSWebDVD.IsSubpictureStreamEnabled(iStream)
```

## <a name="parameters"></a>Parametri

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*Istream*
</dt> <dd>

Specifica il flusso dell'immagine secondaria come integer.



| Valore   | Descrizione              |
|---------|--------------------------|
| Da 0 a 31 | flusso di immagini secondarie        |
| 63      | Flusso a bassa velocità in bit disattivato |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore booleano che indica se il flusso audio specificato è disponibile nel titolo corrente. True indica che è disponibile.

## <a name="remarks"></a>Commenti

Anche se un disco può contenere fino a 32 flussi di immagini secondarie, ogni flusso non è necessariamente disponibile per ogni titolo. Verificare sempre che sia disponibile un flusso per un titolo prima di impostare la [**proprietà CurrentSubpictureStream.**](currentsubpicturestream-property.md)

 

 



