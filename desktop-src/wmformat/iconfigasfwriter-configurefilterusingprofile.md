---
title: Metodo IConfigAsfWriter ConfigureFilterUsingProfile
description: Il metodo ConfigureFilterUsingProfile è la modalità consigliata per impostare un profilo. Configura il filtro per scrivere un file ASF basato sul profilo definito dall'applicazione specificato.
ms.assetid: 278e5109-ba22-4a1c-9c6a-5cfcb9f57d37
keywords:
- Metodo ConfigureFilterUsingProfile Windows Media Format
- Metodo ConfigureFilterUsingProfile Windows Media Format, interfaccia IConfigAsfWriter
- Interfaccia IConfigAsfWriter-formato Windows Media, metodo ConfigureFilterUsingProfile
topic_type:
- apiref
api_name:
- IConfigAsfWriter.ConfigureFilterUsingProfile
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 07b8d87fbf7e8b2d1d46acf55fe96bfdfef472b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300277"
---
# <a name="iconfigasfwriterconfigurefilterusingprofile-method"></a>Metodo IConfigAsfWriter:: ConfigureFilterUsingProfile

Il metodo **ConfigureFilterUsingProfile** è la modalità consigliata per impostare un profilo. Configura il filtro per scrivere un file ASF basato sul profilo definito dall'applicazione specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ConfigureFilterUsingProfile(
  [in] IWMProfile *pProfile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pProfile* \[ in\]
</dt> <dd>

Puntatore all'interfaccia [**IWMProfile**](iwmprofile.md) nel profilo definito dall'applicazione.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT**. I valori possibili includono, ma non sono limitati a, quelli indicati nella tabella seguente.



| Codice restituito                                                                                         | Descrizione                                                   |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <dl> <dt>**\_OK**</dt> </dl>                | Il metodo è riuscito.<br/>                              |
| <dl> <dt>**\_puntatore E**</dt> </dl>           | Puntatore all'interfaccia **IWMProfile** non valido.<br/> |
| <dl> <dt>**\_ \_ stato non corretto di VFW E \_**</dt> </dl> | Il grafico è stato arrestato.<br/>                              |



 

## <a name="remarks"></a>Commenti

Se ha esito positivo, questo metodo provocherà l'invio di un evento di **\_ \_ modifica del grafo EC** all'applicazione. Utilizzare questo metodo per configurare il writer con un profilo della serie Windows Media 9 personalizzato creato (o caricato da un file con estensione prx esistente) utilizzando i metodi di Windows Media Format SDK.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))
</dt> </dl>

 

