---
description: Il metodo put \_ Size imposta le dimensioni di output e la modalità stretch.
ms.assetid: 1186eee4-b5c1-4216-abb3-86ea03b2da40
title: Metodo IResize::p ut_Size (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IResize.put_Size
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: d2da95cca7bf19182dd4c0f5f385715256ae9c5253c356094110c028fb1b016d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117818131"
---
# <a name="iresizeput_size-method"></a>Metodo IResize::p ut \_ Size

> [!Note]  
> \[Deprecato. Questa API potrebbe essere rimossa dalle versioni future Windows.\]

 

Il `put_Size` metodo imposta le dimensioni di output e la modalità stretch.

## <a name="syntax"></a>Sintassi


```C++
HRESULT put_Size(
  [in] int Height,
  [in] int Width,
  [in] int Flags
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Altezza* \[ Pollici\]
</dt> <dd>

Altezza del video, in pixel.

</dd> <dt>

*Larghezza* \[ Pollici\]
</dt> <dd>

Larghezza del video, in pixel.

</dd> <dt>

*Flag* \[ Pollici\]
</dt> <dd>

Modalità di estensione. Per [**i valori possibili,**](resize-flags.md) vedere Flag di ridimensionamento.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un **valore HRESULT.**

## <a name="remarks"></a>Commenti

DES può chiamare questo metodo prima o dopo la **chiamata a put \_ MediaType**. Se DES chiama questo metodo prima di chiamare **put \_ MediaType,** il filtro deve selezionare un valore predefinito per la profondità di bit e usare i valori delle dimensioni per costruire un tipo di supporto di output. Se DES chiama questo metodo dopo aver chiamato **put \_ MediaType,** il filtro deve modificare il tipo di output corrente con le nuove dimensioni.

DES può anche chiamare questo metodo dopo la connessione del pin di output. In tal caso, modificare il tipo di output e riconnettere il pin di output con il nuovo tipo. Per [altre informazioni, vedere Riconnessione](reconnecting-pins.md) dei pin.

Il *parametro Flags* specifica come il filtro deve eseguire l'operazione di ridimensionamento.

> [!Note]  
> Il file di intestazione Qedit.h non è compatibile con le intestazioni Direct3D successive alla versione 7.

 

> [!Note]  
> Per ottenere Qedit.h, scaricare l'aggiornamento di Microsoft Windows SDK per Windows [Vista e .NET Framework 3.0.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h non è disponibile in Microsoft Windows SDK per Windows 7 e .NET Framework 3.5 Service Pack 1.

 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|-----------------------------------------------------------------------------------------|
| Versione<br/> | DirectX 9.0 o versione successiva<br/>                                                         |
| Intestazione<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Libreria<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Codici di errore e di esito positivo](error-and-success-codes.md)
</dt> <dt>

[**Interfaccia IResize**](iresize.md)
</dt> </dl>

 

 




